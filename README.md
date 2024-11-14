

## Predict output data from input data

The data contains sensor and control variables from many machines. 

We focus on a machine called "spannrahmen" for now, you can look it up on the web. 

There are 5 such machines called SP2, SP3, SP4, SP5, SP6 the data points are read once a second with the units in the list below.

Our main optimization parameter is Rest_Fe (left, right and middle), which stands for remaining moisture. 

We try to set the control parameters like speed and temperature in a way to optimize this value.

We can either try to increase speed (to increase throughput with the same energy use) or reduce temperature (to reduce energy use with the same throughput).

As with the other example, the first step is to try to train a model that predicts remaining moisture based on temperature, velocity, possibly other parameters available and also possibly on the type of product being produced (which you can find in the field "artikel"). 

I filtered all data for you already, so you only find data from the SP machines with status "PRODUKTION" (producing).

Its from 01-2022 to 04-2024 in one parquet file per month all tared together to 1.1 GB size file:


### Syllabus:

Frequenz: Frequency – likely referring to the frequency of a process or machine operation.

Breite01, Breite02, …, Breite07: Width Measurements – possibly measurements at different points or stages in the process.

Diff_EA_Ge: Differential Input/Output (Ge) – could indicate the difference between input and output values, with “Ge” possibly indicating a specific parameter or location.

Diff_EA_Me: Differential Input/Output (Me) – similar to above, with "Me" potentially signifying another specific parameter or point.

Duese_vW_Fixomat01, Duese_vW_Fixomat02, …, Duese_vW_Fixomat09:  Nozzle at Pre-Fixomat – refers to different nozzle positions or states in a "Fixomat" machine section.

Geschw_Ausl: Exit Speed – the speed at which materials exit the machine.

Geschw_Einl: Entry Speed – the speed at which materials enter the machine.

Meterz_Ausl: Exit Metering – could refer to the measurement of material quantity or distance as it exits.

Meterz_Einl: Entry Metering – measurement of material quantity or distance as it enters the machine.

Rest_Fe_Li: Residual Moisture Left – moisture content remaining in the material on the left side.

Rest_Fe_Mi: Residual Moisture Middle – moisture content remaining in the material in the middle.

Rest_Fe_Re: Residual Moisture Right – moisture content remaining on the right side.

Sieb_nW_Fixomat01, Sieb_nW_Fixomat02, …, Sieb_nW_Fixomat09: Screen in Fixomat – different screens or mesh positions in the Fixomat machine, potentially related to filtration or separation.

Temp_Regelkreis01, Temp_Regelkreis02, …, Temp_Regelkreis09: Temperature Control Circuit – refers to different temperature regulation circuits, possibly at various locations in the machine.

Geschwindigkeit: Speed – generic term for the speed of a process or machine.

Querzug_1, Querzug_2, Querzug_3, Querzug_4: Cross Pull – likely represents lateral or cross-directional pulling forces or tensions applied to the material.

Reckanzeige_1, Reckanzeige_2, Reckanzeige_3: Stretch Indicator – shows stretch or elongation levels at different stages.

Temp_Feld01, Temp_Feld02, …, Temp_Feld06: Temperature Field – temperature values measured at various fields or points.

Zug_Reck_1, Zug_Reck_2, Zug_Reck_3: Stretch Force – the force applied to stretch or pull the material at different points.

StromL1, StromL2, StromL3: Current (Line 1, Line 2, Line 3) – electric current in phases L1, L2, and L3.

Wirkenergie: Active Energy – the actual energy consumed by the machine, possibly indicating power consumption over time.

Wirkleistung Strom: Active Power Current – real power associated with the electric current, representing energy conversion efficiency.