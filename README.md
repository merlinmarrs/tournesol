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

Make sure not to destroy the Monocrystalline Solar Cells when soldering. They will be destroyed at temperatures higher than 220C (see the datasheet : https://waf-e.dubudisk.com/anysolar.dubuplus.com/techsupport@anysolar.biz/O18AzRx/DubuDisk/www/Gen3/KXOB25-03X4F%20DATA%20SHEET%2020210127.pdf). I used low temperature solder paste and a hot plate to solder these to 3cm pieces of metal wire which I then later solder normally to the PCB.

If this kit is to be given to beginners, I would help them by first soldering the MOSFET, voltage trigger and solar cells.

You can use hot glue to attach the motor to the back of the PCB and 3D print an adapter that fits onto the axel so it stands still or just hot glue it to something.

