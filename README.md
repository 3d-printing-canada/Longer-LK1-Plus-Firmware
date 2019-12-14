# Longer LK1 Plus Firmware
 
In this guide we'll show you how to install and upload firmware and hardware for your BL touch on the Longer LK1/LK2. The standard (non BL touch) firmwares have also been uploaded. There are a couple variations of these printers, so there are some important points we need to note to do the conversion successfully:

# Bill Of Materials
- BL touch: https://3dprintingcanada.com/products/genuine-antclabs-bltouch-sensor
- EX-2000 Extension Cable: https://3dprintingcanada.com/products/genuine-antclabs-bltouch-extension-cables
- BL Touch 3D Printed Mount: https://www.thingiverse.com/thing:3526108

BUY THE COMPLETE KIT: COMING SOON.

# Software Installation (For Standard & BL Touch Firmwares)

1) In the main folder you will see 'LK1 PLUS ##### Firmware' folders. Copy the project.bin file from the desired configuration folder onto your SD card and insert it into the printer. Turn the printer on and watch it upload.
2) When you see the main info screen for marlin appear, turn the printer off. Insert your SD card into your computer again and delete 'project.bin' (failure to do this will mean the firmware will reflash every time). IMPORTANT: You will notice there is now an EEPROM.dat file. DO NOT delete this - as it serves as the Eeprom for your printer (the memory).
3) Re-insert your SD card
4) Configuring the BL Touch

NOTES: 
i) To navigate to a previous menu, you can press the X button on the LCD display
ii) The EEPROM data for the Z probe offset is stored on the SD card. If you start the printer without the SD card in it, that setting will not load properly. Always start your printer with the SD card in it.

# Probe Z offset For BL Touch Configuration

1) Turn on your printer. You will notice you have three controls: two blue navigation arrows and a red select button.
2) Press the select button and use the arrows to nativage to 'Temperature'.
3) Select 'Preheat PLA' from the list, then 'Preheat PLA' from the next menu. This will preheat the printer.
4) Press the select button and use the arrows to navigate to 'Motion'.
5) Select 'Auto Home'. The printer should home and end up in the center of the bed.
6) In the 'Motion' menu, select Move Axis > Move Z > 10mm. Move the axis down until it is at +000.0 mm.
7) Navigate to the main menu. Go to Configuration > Probe Z offset
8) Put a piece of paper under the nozzle. Move it back and fourth continuously. Press the blue down button and the gantry will slowly start to move down. You may keep your finger on the button.
9) Once the nozzle grips the paper enough that it makes a little resistance, but the paper can still move, press the red select button. Scroll down in the 'Configuration' menu until you reach 'Store Settings'. Select that a couple times just to be sure. You're done!

# Configuring Ultimaker Cura Slicer

Configure the machine in cura with a preset for the Creality CR-10S5, the profile should be exactly the same as the LK1 plus. Please note that for a BL touch configuration, under machine settings you must place a 'G29' after your G28 in the start Gcode on a new line. This will enable auto bed leveling. 
