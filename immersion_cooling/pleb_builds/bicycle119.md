### Goals 
* Have fun and learn all about mining!
* Enjoy time spent with my kids building this ultimate STEM project, they loved it!
* Make my money back invested in these materials over the next ~2 years stacking sats, not in any hurry!

### Summary of Setup
* Miner:  Whatsminer M30S, 88TH with immersion firmware from Whatsminer; but no overclocking firmware is available anywhere I can find.
* Cooling Design:  Single Phase, Dual Loop 
* Coolant:  BitCool
* Electric Service:  Dedicated 100A sub-panel with 'whole house' surge protector, currently has 240V 20A Breakers to L6-20R outlets

Videos of my tank and aircooler are posted on Reddit and in the Telegram threads mentioned below.

### Coolant Loop
* 20 Gal High Glass Fish Tank	$24.00	https://www.petco.com/shop/en/petcostore/product/aqueon-20-gallon-standard-glass-aquarium-tank	
* 10Gal BitCool Coolant	$360	Engineered Fluids	
* Submersible Pump	$58	https://www.amazon.com/dp/B000X07GQS/ref=cm_sw_r_tw_dp_08FW16JB91VWQ5PP4F60?_encoding=UTF8&th=1	
* Acrylic Sheets to Partition Tank	$20	Home Depot; sub divided tank into 3 sections: 1 for overflow and pump, middle section for the miner, 3rd section for possible future miner but more importantly didn’t have to buy 10 more gallons of BitCool!	
* 1" Black Steel Pipe, Elbows and Spacers	$20	Home Depot; used to connect between the plate heat exchanger and CPVC Pipe	
* 1" CPVC, 10ft plus elbows and threaded connectors	$75	CPVC was as EXPENSIVE as copper at the time of my build and hard to find; but made it very easy to cut and assemble flow manifold for the miner vs copper.	
* 30 Plate Heat Exchanger	$99	https://www.vevor.com/products/30-plate-water-to-water-heat-exchanger-oil-cooling-heating-cooling-1-fpt-brazed?variant=32052806811746	

### Air-Cooled Water Loop
* Grundfos UPS15-58FC Water Pump	$109	https://www.outdoorfurnacesupply.com/
* 18"x18" Water-Air Radiator	$159	https://www.outdoorfurnacesupply.com/
* Air Cooler Enclosure	$50	Lumber:  Two 2x12x10ft from Home Depot, One 2x4x8ft
* 3000cfm DC Fan	$45	https://www.amazon.com/dp/B01MTLGP1Q?psc=1&ref=ppx_yo2_dt_b_product_details
* PWM DC Motor Speed Controller	$17	https://www.amazon.com/dp/B00JEXJXAC?psc=1&ref=ppx_yo2_dt_b_product_details
* 12V 15A 180W Power Supply 	$19	https://www.amazon.com/dp/B078RZ6C3N?psc=1&ref=ppx_yo2_dt_b_product_details
* 1" PVC and fittings for Cold Water return	$20	Total of 30' between plate heat exchanger to air cooler outside
* 1" CPVC and fittings for Hot Water out	$150	Total of 30' to get hot water out to Air Cooler outside.  I wasn't sure how hot the water was going to get from the Coolant loop via heat exchanger so played it safe, although it cost A LOT more than PVC for the return cold water.

There were other supplies and tools but nothing major, I reused a lot of what I had from other non-related projects over the years.

It's been working great for 2 months now, just one leak so far and just playing with various pools  (slush, poolin, etc) and miner management platforms (Foreman.mn, HiveOS and minerstat).

Total Watts for the 2 pumps and the fan to keep the miner temps at 40C:  249W measured with outlet watt meters

### Next Up
* Add a PID / PLC Controller to automatically control the air cooler fan speed based on the temperature of the Bitcool in the tank or outside temp, not sure yet (I'm dong it manually now via the PWM speed controller)
* Tie into my furnace to heat the house and hot water.
* Add another miner
* Find and install Whatsminer M30S overclocking firmware

This is the place to start for all things DIY immersion:   https://github.com/satoshi-anonymoto/pleb-miners/blob/main/immersion_cooling/README.md 

I don't recall exactly how I came to find all this info but my first 2 Youtube videos I ever watched on the topic were CoinHeated's setup (https://www.youtube.com/channel/UCDnDC-nakOgpp0zLbUOvQIw/featureD) and Neetbux Labs Ammo Can Immersion setup (https://www.youtube.com/channel/UC7fFZl-4CCu5MEwT9sDwvxw/videos) 

I then found my way over to Telegram https://t.me/ImmersionCoolingTechnologyTalk and referenced this Reddit thread quite a bit as well. https://www.reddit.com/r/Immersion_Cooling/   

The rabbit hole is deep and complex…have fun!
