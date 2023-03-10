---
title: Baby, it's cold outside!
description: How are you and your neighbors staying warm this winter? Mapping heating across US states
---

<meta property="og:image" content="/assets/us-electric-heating.png" />

How are you and your neighbors keeping your homes warm this winter? The answer depends on where in the US you live. Over half of US households heat their homes by burning fossil fuels-- most of these households use natural gas, but some use fuel oil, kerosene, or propane. In other parts of the country, households use electricity to heat their homes. How common are these different heating methods across the US, and what drives these differences?

To answer these questions, I used data from the US Energy Information Agency's [2020 Residential Energy Consumption Survey](https://www.eia.gov/consumption/residential/data/2020/). Every few years since 1978, US Energy Information Agency, part of the Department of Energy, has surveyed people across the country about how they use energy in their homes, including how they heat their house. State-wide data is available about the share of households that use natural gas, propane, fuel oil or kerosene, and electricity as their main heating fuel. (Data about other heating fuels, such as wood, were not available.) Let's look into the how residential heating varies by state and some of the factors driving those differences.

## Natural gas
Natural gas is the dominant heating fuel in the US: 46% of households use it as their main heating fuel. As shown in the map below, natural gas is most prevalent across Mid-Atlantic, Midwest, Great Plains, and the Southwest. Natural gas is less common as the main heating fuel in northern New England, the Southeast, and the Pacific Northwest. Two factors driving these differences across states are heating needs and residential access to the gas grid.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~clairehalloran/3.embed" height="525" width="100%"></iframe>

I estimate heating needs in each state using heating degree days. This metric captures the difference between a desired indoor temperature and the outdoor temperature and how long that difference lasts in days. For example, if the average outdoor temperature on a day is 35 degrees F and the desired indoor temperature is 65 degrees, there are 30 degree-days that day. Heating degree days are only counted when it's colder outside than inside. I use the total 2020 heating degree days for the lower 48 states from [NOAA National Centers for Environmental information, Climate at a Glance](https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/statewide/mapping/110/hdd/202012/12/value). A higher number of heating degree days indicates that the state needs more energy for heating.

Some households may not use natural gas heating because they don't have access to the natural gas distribution grid. To quantify gas grid access in each state, I estimated the share of each state's population that lives within a [natural gas local distribution company service territory](https://hifld-geoplatform.opendata.arcgis.com/datasets/geoplatform::natural-gas-local-distribution-company-service-territories/explore?location=38.832184%2C-112.428215%2C3.82) using [2010 US population density data](https://data.usgs.gov/datacatalog/data/USGS:57753ebee4b07dd077c70868). (This population density data is only available for the contiguous US.) I compared the population within a distribution company service territory with the total  [2010 census population](https://www.census.gov/data/tables/time-series/demo/popest/2010s-state-total.html) of each state and the District of Columbia. Because this is a rough estimate of the percent of the population living within a distribution company territory, some states have values slightly above 100%.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~clairehalloran/13.embed" height="525" width="100%"></iframe>

Plotting these data shows a clear correlation between heating degree days and the prevalence of natural gas heating: natural gas heating is more common in colder areas. However, there are some exceptions to this trend. Vermont, Maine, and New Hampshire are all cold states where less than one-third of households use natural gas as their main heating fuel. These New England outliers can be explained by a lack of access to natural gas: all of these states have their low shares of population living within a natural gas distribution company service territory.

Another group of outliers are some of the coldest states in the lower 48: North Dakota, Minnesota, Montana, Wyoming, and South Dakota. Despite widespread access to natural gas networks in these Great Plains states, as indicated by high shares of their population living within a natural gas distribution company service territory, a lower share of households in these states use natural gas as their primary heating fuel. 

## Other fossil fuels
While natural gas is the most common fossil fuel for heating homes in the US, some households use propane, fuel oil, and kerosene instead. Four percent of households use propane as their main heating fuel, and 4% use fuel oil or kerosene. While these numbers are small on the national scale, these fuels dominate in some areas.

The map below shows that propane is most common in northern New England and the Upper Midwest and the Great Plains, especially Minnesota, North Dakota, and South Dakotas. Even in these states, only 13 to 15% of households use propane as their main heating fuel.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~clairehalloran/7.embed" height="525" width="100%"></iframe>

As shown in the map below, fuel oil or kerosene heating is most prevalent in New England and Alaska. Over 40% of households in Vermont, New Hampshire, and Maine use these fuels as their main heating fuel, possibly driven by a lack of access to the gas grid. 

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~clairehalloran/9.embed" height="525" width="100%"></iframe>

These other fossil fuels are most common in state are outliers in the the previous scatter plot: cold places that have fewer households than expected using natural gas as their main heating fuel. Many households in northern New England don't have access to the gas grid, so they use fuel oil, kerosene, or propane for heating instead. Some of the coldest states in the Great Plains that have fewer households than expected using natural gas have some households using propane heating instead.

## Electric heating
Electricity is the second most common heating fuel in the US, with 40% of US households using it as their main heating fuel. As shown in the map below, electric heating is most common in the Southeast and Pacific Northwest and least common in New England and the Midwest. Let's look at some of the factors related to these geographic trends: heating needs and the residential electricity prices.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~clairehalloran/1.embed" height="525" width="100%"></iframe>

As seen in the plot below, there is a clear correlation between heating degree days and electric heating: electric heating is more common in warmer states. While each unit of heat from gas is usually cheaper than heat from electricity, electric furnaces are typically cheaper than gas furnaces. This initial cost difference means that electric heating can be cheaper overall in warm climates where little heating is needed.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~clairehalloran/11.embed" height="525" width="100%"></iframe>

The influence of [2020 electricity price](https://www.eia.gov/electricity/state/archive/2020/) on the prevalence of electric heating is clear in the plot above.  Residential electricity price can explain why places with similar heating needs, as measured by heating degree days, have large differences in the share of households using electric heating. For example, in California, with average 2020 residential electricity prices of 20.45 cents per kilowatt hour, only 28% of households use electricity as their primary heating fuel, compared to Georgia, where 2020 average electricity prices were 12.1 cents per kilowatt hour, 53% of households use electricity as their primary heating fuel. Georgia had 2,379 heating degree days in 2020 and California had 2,564. The colder states of Washington and New York both had 5,425 and 5,499 heating degree days, respectively. However, residential electricity prices were much cheaper in Washington, where only 58% of households use electricity as their main heating fuel, than in New York, where 20% of households use it. Low electricity prices also contribute to the prevalence of electric heating in cold states on the Great Plains.

## Heat pumps
While most electric heating in the US is resistance heating, 14% of households use highly efficient heat pumps to keep their homes warm. Heat pumps move heat from the outside to inside the house, so they can move up to 3-5 units of heat inside for every unit of electricity they use. In contrast, resistance heaters use 1 unit of electricity to create 1 unit of heat. 

As seen in the map below, heat pumps are most common in the Southeast. South Carolina has the highest share of residential heat pumps, with 46% of households using one to stay warm. In contrast, they  are relatively uncommon in the Northeast, Midwest, and West, with the exception of Arizona. (For states in gray, heat pump data were withheld because either the relative standard error (RSE) was greater than 50% or there were fewer than 10 households in the reporting sample.)

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~clairehalloran/56.embed" height="525" width="100%"></iframe>

One of the most effective ways to reduce your household carbon emissions is switching your heating system to a heat pump. Space heating accounted for 43% of energy use in US homes in 2015 according to the [US Energy Information Administration](https://www.eia.gov/energyexplained/use-of-energy/homes.php), so using a more efficient, less carbon-intensive heating system can make a big impact. [One 2021 study](https://iopscience.iop.org/article/10.1088/1748-9326/ac10dc) found that heat pump adoption reduces carbon dioxide emissions for 70% of US houses, assuming that electric grid carbon dioxide emissions decrease by 45% over the next 15 years. Notably, the number of households that can reduce their carbon emissions by switching to a heat pump is higher if the US reaches its [goal of 100% carbon-free electricity by 2035](https://www.whitehouse.gov/briefing-room/statements-releases/2021/04/22/fact-sheet-president-biden-sets-2030-greenhouse-gas-pollution-reduction-target-aimed-at-creating-good-paying-union-jobs-and-securing-u-s-leadership-on-clean-energy-technologies/). Efficient electric heating and clean electricity are key for reducing emissions from residential heating.

## Conclusion
How you heat your home depends mostly on the weather in your state: natural gas is more common in colder states and electricity is more prevalent in warmer states. If you live in a state like Vermont, Maine, or New Hampshire, where many households do not have access to the gas grid, you might turn to other fossil fuels, including fuel oil, kerosene, and propane, to heat your home. Residential electricity prices also play a role: if you live in a warm state with high electricity prices, like California, you're more likely to use natural gas instead of electric heating. On the other hand, if you live in a temperate state with low electricity prices, such as Washington, you're more likely to use electric heating than residents of states with a similar climate and higher electric bills. 

Heating is the largest energy use in US homes, and reducing emissions from heating is a key part of averting the worst impacts of the climate crisis. While high-efficiency electric heat pumps are currently only widespread in the Southeast, the majority of households across the US can reduce their emissions from heating by switching to a heat pump. Let's stay warm this winter without heating our planet!

### About the author
[Claire Halloran](https://clairehalloran.github.io/) is a doctoral candidate in energy systems engineering at the University of Oxford.
