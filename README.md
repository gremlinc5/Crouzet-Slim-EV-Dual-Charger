# Crouzet Slim - EV Dual Charger
New Crouzet Slim used to charge dual EVs with timing and sensing to stop charging at wanted kWh. Normal portable charging assets ca be used to charge from normal plugs.

PLC software sense the main power and the single current of the two EV's plugs. The forth input is a dry contact to ask the PLC to mantain plugs powered like normal wall plugs.

The four relays are used in parallel to maximize the output current as Crouzet PLC Slim Datasheets states: O1-O2 at 10 Amps and O2-O3 at 8 Amps. Search for right value if changed by Crouzet.

In the menu system, measures can be seen in page 0. "A" and "B" buttons are used to move between pages, "plus" and "minus" are used to change values.

Page 1 and 2 are for entering the main current histeresis values for charge stop and restart. Avoids main interruptor to open.

Page 3, 4 and 5 are for entering the EV1 energy needed and timing values.

Page 6, 7 and 8 are for entering the EV2 energy needed and timing values.

In page 3 and 6 stored needed value will be set when start hour is hit, or if you want to set more charges a day you can hit "OK" button to load needed value to current counter.

Page 9 will set EV priority: first EV priority, second EV priority, same EV priority will cycle between EVs 1 hour each, all EVs priority will try to load EVs simultaneously.

Page 10 and 11 are used to set timing mode for EV charging, timing mean that charge will start after Start Hour and stops at Stop Hour and will load only Needed kWh value to the EVs.

Software is in 0.1 version beta "as is" with no warranty, you can simulate it with Crouzet Soft to understand if you like it.

On field ChargeTransferFunction.csv needs to be reloaded in Function f(x) blocks, current block is in test mode with timings 1/10.

Protection addition is needed for EV charging, check with you electrician what you need to protect your home in your country.