# Immersion Cooling
The most effective way to keep your ASICs at a constant, consistent temperature is to run them fully submerged in a special liquid that pumps the heat out to heat exchangers. The bonus side effect is that the ASICs run silently in the liquid with only a heat exchanger fans running outside.

Most of the information here was gleaned from the [Immersion Cooling Technology Talk](https://t.me/ImmersionCoolingTechnologyTalk) Telegram group.

Also from discussions in this [twitter thread](https://twitter.com/SatoshiAnon/status/1431610380212637704).


### Does immersion cooling make sense for you?
If you're running a single S9 that you bought for $450, no. Unfortunately the cost for even the simplest immersion cooling setup is probably around $300-400. For a single 3kW ASIC ($4k-10k!) it's easier to justify the costs.


## Terminology
* dielectric fluid: a liquid that doesn't conduct electricity and is therefore safe to submerge electronics in. These are very expensive, custom manufactured oils.

* single loop: The cooling oil is directly pumped through a radiator to cool it down and then fed back into the ASIC reservoir.

* double/dual loop: The cooling oil is pumped to a plate heat exchanger where it transfers heat to an adjacent water line. The heated water is then pumped in its own loop to a radiator to cool it down.

* single phase: The cooling oil always stays in a liquid state as it's pumped around the system.

* dual phase: The cooling oil is boiled off by the hot electronic components and that resulting gas is captured and cooled so that it condenses back to a liquid. This is not for the plebs!


## Basic design tradeoffs - single loop
Single loop is the simplest and least expensive option for small pleb setups.

pros:
* Simple. Only need a container, the expensive cooling oil, one strong enough pump, a modest radiator, fan, and some misc hoses and connectors.
* Lower starting costs since there isn't much hardware to buy.

cons:
* Pumping the oil through all the radiator loopbacks is difficult so you have to spec out the pump appropriately.
* Radiator is less efficient at shedding heat when filled with oil instead of water (probably due to difficulty of pumping it through? Faster water flow = better cooling? Or inherent property of the cooling oil vs water?)
* Uses more oil (most expensive part of any system) than a double loop system.
* Need to keep the hose lines short to minimize amount of oil that has to be pumped around; limits installation options.
* Will quickly hit a practical limit where it can't dissipate enough heat. If plebs think they'll want to scale up over time, better to just go double loop from the start.


## Basic design tradeoffs - double loop
A must for any immersion setup at scale, but also has some compelling reasons for small-scale plebs.

pros:
* Minimizes the total cooling oil needed in the system.
* Water is easier to pump so longer runs to the radiators are more practical.
* Only real option once setups go beyond 1-2 high power (3kW+) ASICs (really rough guess).
* Easier to incorporate into home heating uses (I think?).

cons:
* Higher initial starting costs. Oil pump needed (though can have much more modest specs), water pump, plate heat exchanger block, then all the same radiator, fan, hoses, etc.
* Some seasonal water mix adjustments for freezing temps.


## Cooling parameters, data, design considerations
* S19s reach thermal shut down at [160-170°F oil temps](https://t.me/ImmersionCoolingTechnologyTalk/16504)
* Plebs report steady-state oil temps around 125F, chips in the low 70°C.
* Engineering Fluids guidelines state 2-4L/min per kW for minimum oil circulation rate.
* Oil flow through the ASIC is key. Some miners [leave the case fans on](https://t.me/ImmersionCoolingTechnologyTalk/15448) to generate flow.
* Oil-to-water [plate heat exchanger efficiency](https://t.me/ImmersionCoolingTechnologyTalk/16376): 120°F oil input heats the water to 110°F

### Guesstimating oil & water pump requirements
Guesstimating oil pump capabilities: Let's double the 2-4L/min per kW guideline. And then add another 25% buffer. Then assume the pump's flow rate is cut in half by pumping the thicker cooling oil.

So for a 7.2kW system (two Whatsminer M31s+):

`7.2 * 4*2 * 1.25 / 3.785L/gal * 60min/hr * 2 = 2282 gal/hr`

In theory, [this fairly cheap 2600gph submersible pump](https://www.amazon.com/VIVOSUN-Submersible-Waterfall-Statuary-Hydroponic/dp/B07FJWM52K) should suffice.

The water pump math will depend on the size of the radiator. I don't have a good starting point here, other than that I'll be aiming for ~8gpm and then size the radiator accordingly (somehow).


## Containers
Remember that the cooling oil is the most expensive part of the system. Do not cut corners on a container that may end up leaking your oil!

There are a few DIY options listed to build your own container. Unless you can find the perfect pre-made container that checks off all the boxes 

### Fish tanks
Have been used for quick, short-term experiments and in some plebs' main setups. Some concerns about the durability of corner joins holding up to the hot oil over time but [at least one report](https://t.me/ImmersionCoolingTechnologyTalk/16504) of the silicon edge seals being compatible with BitCool.

### Off-the-shelf metal containers
Huge array of possibilities here. Steel or alumninum [don't have any issues](https://t.me/ImmersionCoolingTechnologyTalk/16524) interacting with the cooling oil. Again take care to pay attention to any seams.



## Sample builds
[CoinHeated's double loop pool heating system](pleb_builds/coinheated.md)
