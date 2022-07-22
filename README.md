# Tournesol

A mini BEAM photo head (a.k.a. sunflower) that orients itself towards the sun. 

All the component selection work done by Nick Ames here: https://www.fetchmodus.org/projects/beam/photopopper/ 

The idea to use two solar panels and the midpoint instead of phototransistors comes from Simon Fraser here : http://www.smfr.org/robots/robot_images/dualsolarhead_schematic.png

My documentation of making the device here: 
https://www.marrs.io/dual-solar-tracking-part-iii/

https://www.marrs.io/sunflower-array/



# BOM from Mouser and Digikey: 

74AC240 (make sure it's the AC flavour as it must work at low voltages): 

https://www.mouser.fr/ProductDetail/Texas-Instruments/CD74AC240M96?qs=YxwvVplHM%2FkSs49pJJGWDg%3D%3D

0.15F cap :

https://www.mouser.fr/ProductDetail/Panasonic/2R5TPE1500MC?qs=OE1iw1LrrPHN6IeHWYVhLw%3D%3D

diode (standard 1206)

0.47uF cap (standard 1206)

x2 2.23 V Monocrystalline Solar Cell (to get above the trigger voltage in full sunlight):

https://www.digikey.fr/en/products/detail/anysolar-ltd/KXOB25-03X4F-TR/13999191

micro gear motor (make sure it works as low as 2.9V): https://www.mouser.fr/ProductDetail/DFRobot/FIT0094?qs=lqAf%2FiVYw9h6rFbdWMR0RQ%3D%3D

voltage trigger (2.9V but you can try other values): https://www.mouser.fr/ProductDetail/Renesas-Intersil/ISL88001IH29Z-T7A?qs=dAsayXGOMrvzqg4LBGVqAg%3D%3D

N-channel MOSFET: https://www.mouser.fr/ProductDetail/Diodes-Incorporated/DMN2215UDM-7?qs=ptj1V1atRArXZWZ7Y9ryoQ%3D%3D

# THINGS TO WATCH OUT FOR:

These components aren't super common (especially the solar cells) and they aren't super inexpensive either (especially the solar cells again, but also the 0.15F capacitors). 

Make sure not to destroy the Monocrystalline Solar Cells when soldering. They will be destroyed at temperatures higher than 220C (see the datasheet : https://waf-e.dubudisk.com/anysolar.dubuplus.com/techsupport@anysolar.biz/O18AzRx/DubuDisk/www/Gen3/KXOB25-03X4F%20DATA%20SHEET%2020210127.pdf). I used low temperature solder paste and a hot plate to solder these to 3cm pieces of metal wire which I then later solder normally to the PCB (see photo of final tournesol).

If this kit is to be given to beginners, I would help them by first soldering the MOSFET, voltage trigger and solar cells.

You can use hot glue to attach the motor to the back of the PCB and 3D print an adapter that fits onto the axel so it stands still or just hot glue it to something.

In order to test that the solar panels are functioning, you need a nice inefficient incandescent light - not a super efficient LED light. Better yet, the sun at midday in the summer! To test turning right and left, you can cover 1/5 of one of the solar panels and it should turn away from the dark side. If it does the opposite, just change the wiring of the motor. You'll need to mess around with the tilting of the two solar panels, if they are too tilted away from one another they won't both get enough sun to get over the 2.9V trigger level. If they are both pointing straight ahead, you might get less good sun seeking. 
