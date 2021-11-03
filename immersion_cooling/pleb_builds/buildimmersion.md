# BuildImmersion's (planned) single asic build

A single loop immersion system for S19s or M30s (or equivalent asics) with a focus on build quality (reliability), temperature and protection control (able to run unsupervised "forever"), negligible noise (slightly oversized heat exchanger / fan so that the fan will never need to run on max), flexible placement (inside or outside, heat exchanger placed by tank or externally), heat reuse as is (air) or connected to water heating system by water-to-water heat exchanger.

Detailed library of documentation can be found [here](https://keybase.pub/evenutstrand/) as system is getting as-built (continually updated).

* [DCX ThermaSafe R dielectric fluid](https://cryptocooling.eu/#fluid), two 25l containers: $482 ($241 per container, $9.64 per litre)
* Tank will be custom made. Drawings can be found [here](https://keybase.pub/evenutstrand/Tank%20Drawings/). Estimated cost: ~$700
* Circulator pump to be determinded (TBD), but will start out with a used [Grundfos Alpha2 25-80 180 (~$250, 50W)](https://product-selection.grundfos.com/products/alpha/alpha2/alpha2-25-80-180-98649757?tab=variant-curves) that I came across, read off flow and power parameters from its display, and calculate needed pump size from there. I estimate that a variant of [Grundfos Magna3](https://product-selection.grundfos.com/products/magna/magna3?tab=models) is needed: ~$600, 100-200W
* [16x16" heat exchanger](https://www.outdoorfurnacesupply.com/16x16-water-to-air-heat-exchanger-hot-water-coil-outdoor-wood-furnace.html): $149
* Custom made fan shroud for above heat exchanger. Drawings can be found [here](https://keybase.pub/evenutstrand/Fan%20Shroud%20Drawings/). Estimated cost: ~$250
* [350mm axial fan](https://ventilatorry.ru/downloads/ebmpapst/datasheet/s3g350-ag03-52-en-datasheet-ebmpapst.pdf). Purchased directly from manufacturer (ebm-papst): ~$350, <85W
* [PID 0-10v speed controller for fan](https://www.alliedelec.com/product/red-lion-controls/pxu40030/71103615/): ~$140
* Other electrical and control components: ~$700
* Miscellaneous: ~$500

Total: ~$3871 + shipping etc.

Power consumption (estimated): 150W
