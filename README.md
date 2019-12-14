# Longer LK1 Plus Firmware
 
In this guide we'll show you how to install and upload firmware and hardware for your BL touch on the Longer LK1/LK2. The standard (non BL touch) firmwares have also been uploaded. There are a couple variations of these printers, so there are some important points we need to note to do the conversion successfully:

# Bill Of Materials
BL touch: https://3dprintingcanada.com/products/genuine-antclabs-bltouch-sensor
EX-1000 Extension Cable (For Longer LK2 / Alfawise U30 V0G MOTHERBOARD ONLY): https://3dprintingcanada.com/products/genuine-antclabs-bltouch-extension-cables
BL Touch 3D Printed Mount: https://www.thingiverse.com/thing:3526108
BUY THE COMPLETE KIT: https://3dprintingcanada.com/products/longer-lk2-alfawise-u30-bl-touch-kit This kit comes with everything you need for the modification, including a pre-soldered extension cable with integrated resistor

# Software Installation (For Standard & BL Touch Firmwares)
In the main folder you will see a '####_firmware.bin' file. Copy that folder onto your SD card and insert it into the printer. Turn the printer on and watch it upload.
When you see the main info screen for marlin appear, turn the printer off. Insert your SD card into your computer again and delete '####_firmware.bin' (failure to do this will mean the firmware will reflash every time). IMPORTANT: You will notice there is now an EEPROM.dat file. DO NOT delete this - as it serves as the Eeprom for your printer (the memory).
Re-insert your SD card
Configuring the BL Touch
NOTES: i) To navigate to a previous menu, you have to scroll to the top of your current menu and press the topmost option ii) The EEPROM data for the Z probe offset is stored on the SD card. If you start the printer without the SD card in it, that setting will not load properly. Always start your printer with the SD card in it.

Turn on your printer. You will notice you have three controls: two blue navigation arrows and a red select button.
Press the select button and use the arrows to nativage to 'Temperature'.
Select 'Preheat PLA' from the list, then 'Preheat PLA' from the next menu. This will preheat the printer.
Press the select button and use the arrows to navigate to 'Motion'.
Select 'Auto Home'. The printer should home and end up in the center of the bed.
In the 'Motion' menu, select Move Axis > Move Z > 10mm. Move the axis down until it is at +000.0 mm.
Navigate to the main menu. Go to Configuration > Probe Z offset
Put a piece of paper under the nozzle. Move it back and fourth continuously. Press the blue down button and the gantry will slowly start to move down. You may keep your finger on the button.
Once the nozzle grips the paper enough that it makes a little resistance, but the paper can still move, press the red select button. Scroll down in the 'Configuration' menu until you reach 'Store Settings'. Select that a couple times just to be sure. You're done!

# Configuring Cura
Cura configuration is the same as the Ender 3 cura config - please refer to our video below for the procedure: https://youtu.be/dRgWrepDUBE?t=1316

Please note: The Ender 3 configuration will work for the LK2, but for the LK1 you should select the "CR-10" default profile and add a G29 to it as per the instructions in the Ender 3 cura config video above.
