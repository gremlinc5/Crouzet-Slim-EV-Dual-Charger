# Crouzet Slim - EV Dual Charger
New Crouzet Slim PLC used to charge dual EVs with timing and sensing to stop charging at wanted kWh. Normal portable charging assets can be used to charge from normal plugs.

PLC software sense the main power and the single current of the two EV's plugs. The forth input is a dry contact to ask the PLC to mantain plugs powered like normal wall plugs, if PLC Digital Input is a passive one connect 24 volt to the dry contact instead GND.

The four relays are used in parallel to maximize the output current as Crouzet PLC Slim Datasheets states: O1-O2 at 10 Amps and O2-O3 at 8 Amps. Search for right value if changed by Crouzet. External Relays are recomended for currents higher than those listed, check with your electrician what is better.

In the menu system, measures can be seen in page 0. "A" and "B" buttons are used to move between pages, "plus" and "minus" are used to change values.

Page 1 is for seeing kWh to be charged remaining.

Page 2 and 3 is the current histeresis for main power protection: MIN is the current at the charging process restart, MAX is the current at the current charging process pauses.

Page 4 and 5 are the hours at the PLC will reload the kwh needed to the power counter for next night recharging.

Page 6 enable the timers, timer will charge to EVs only the requested energy and starts at start hour.

Page 7 and 8 is probably the timed energy daily wanted to be charged to EV. Setting this parameter in Timing mode permit to not reach higher percentage of the battery unwanted, eg you can load battery to 80% not 100% all days.

Software is in 0.2 version beta "as is" with no warranty, you can simulate it with Crouzet Soft to understand if you like it.

On field ChargeTransferFunction.csv is for normal usage timings, ChargeTransferFunctionTest.csv is for test purposes.

Protection addition is needed for EV charging, check with your electrician what you need to protect your home in your country.

Crouzet Soft used version 1.12.02
