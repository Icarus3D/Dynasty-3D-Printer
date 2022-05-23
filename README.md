# Dynasty CoreXY 3D Printer
![Dynasty_Final_Render](https://github.com/Graysson94/Dynasty-3D-Printer/blob/main/Gallery/Dynasty_Scene_Ortographic.PNG)

After having modified my printers a lot and tested several DIY printer kits like Voron and BLV MGN Cube, I wanted a printer that totally met my needs.
I saw printers on the market that could correspond to my needs by modifying them. But I decided to challenge myself by developing my own printer.
After several months of work, here is the result.
This project was originally intended to be personal only, but I thought that making the files open source might motivate other people to start developing their own 3D printer.

:warning: Warning :warning:<br />
This printer is still at the prototype stage and is not optimized. The cost is quite high and the machine also takes a lot of space
If you want to build a 3D printer by yourself, I recommend the [Voron](https://www.vorondesign.com/) or [RatRig](https://v-core.ratrig.com/) printers which have a great community ready to help you.

If you are interested in my work, you can follow me on Instagram [@icarus_3d](https://www.instagram.com/icarus_3d/?hl=fr). I will post news about my future projects in 3D printing.

## Features List
* Print volume 300x300x360mm
* CoreXY kinematic
* Easy maintenance
* Sturdy Structure with 2040 Aluminium Profiles
* Good speed and print quality (Good result at 100mm/s @ 3k accel)
* Accepts spools of 2kg
* Electronic Bay
* Full enclosure
* Direct drive extruder
* Filament fault detector
* Purge Bucket
* Bed thermal expension compensation
* LED strip
* Auto bed leveling
* Access to the printer outside a local network
* Streaming video
* Timelapse
* Automatic power off after print completion

## Frame
![Dynasty_3D_Printer](https://github.com/Graysson94/Dynasty-3D-Printer/blob/main/Gallery/Dynasty_3D_Printer.JPG)
2040 aluminum profiles are used to obtain a rigid structure.
All corners use 3mm aluminum plates coupled with M6 screws directly screwed to the profiles as hidden joints.
The structure is very rigid, but it requires a lot of screws.
The printer, which is very heavy, is about 85cm high.
All electronic components are installed in the electronic bay on the left side of the printer. The panels on the front, bottom, top and back of the electronic bay are 3D printed.
The enclosure is made of transparent and matte black 3mm plexiglass. Except for the plate on which is fixed the electronics, which is 4mm thick.
Thanks to [coldzero.eu](https://www.coldzero.eu/) for the awesome [Custom Dynasty Panels Kit](https://www.coldzero.eu/custom-dynasty-panels).

## Motion System
![Dynasty_XY_Carriage](https://github.com/Graysson94/Dynasty-3D-Printer/blob/main/Gallery/Dynasty_Carriage.JPG)
The moving system is an XY core system. The two motors used for the movement of the print head are placed at the back of the printer.
The Y-axis uses two linear rails and the X-axis uses one linear rail fixed on a carbon tube.
The head is moved by a 9mm 2GT belt.

![Dynasty_Hotend](https://github.com/Graysson94/Dynasty-3D-Printer/blob/main/Gallery/Dynasty_Hotend.JPG)
The carriage of the hotend is an [EVA](https://main.eva-3d.page/). This is the same carriage platform used for the RatRig printers.

## Bed
![Dynasty_Bed](https://github.com/Graysson94/Dynasty-3D-Printer/blob/main/Gallery/Dynasty_Bed_Support.JPG)
The bed used is a 329x329x6mm cast tooling plate from RatRig.
There is a magnetic plate on top with a flexplate powder coated PEI.
The bed can be heated up to 110°C with a 750W heating pad.
It has three attachment points, each resting on a 3D printed support.
The fixation between the bed and the supports is made with steel balls screwed to the bed and attracted by magnets fixed on the supports.
This system allows to compensate the effects of the thermal expansion of the plate during the heating process. This avoids deformations of the bed caused by the stress. Steel rods guide the balls to ensure the stability of the bed.
The supports are screwed to linear rails and are moved by TR8 lead screws and Nema17 motors. 
These three motors, coupled with the BLTouch sensor, allow the automatic leveling of the bed . There is a link to a [video of the start gcode macro](https://www.youtube.com/watch?v=Yhw2lbUx1_E&t=1s).

## Electronics
![Dynasty_Open_Bay](https://github.com/Graysson94/Dynasty-3D-Printer/blob/main/Gallery/Dynatsy_Open_Electronic_Bay.JPG)
All the electronic components are installed in the electrical bay. Each component is fixed on a 35mm DIN rail with a bracket. The cables are all stored in a 40mm wiring duct.
The electrical bay allows easy access to all electronics and protects the components from the temperature of the printing area.
The printer has a 230V socket at the back. This is directly connected to the emergency stop button on the front panel.
The shutdown button is connected in parallel with the main SSR. Once the printer is switched on with the button, the SSR takes over and the printer can be switched off either via the web interface or directly with the emergency stop button.
The 24V power supply powers the Octopus V1.1 motherboard and the 5V power supply powers the Rapsberry Pi. Most of the components are connected to the motherboard except for the screen and the webcam. The details of the connections are explained in the [Wiring Diagram](https://github.com/Graysson94/Dynasty-3D-Printer/tree/main/Wiring%20Diagram) folder.

## Firmware
![Mainsail_Screenshot](https://github.com/Graysson94/Dynasty-3D-Printer/blob/main/Gallery/Mainsail_Screenshot.PNG)
The printer uses the [Klipper firmware](https://github.com/Klipper3d/klipper).
You can use third-party Moonraker components that allow you to add other functionalities.
Like the [Moonraker timelapse](https://github.com/mainsail-crew/moonraker-timelapse) feature that allows you to make timelapse videos of your prints very easily. This feature was very useful for me to understand the failures of my first prints.
There is also a [Moonraker bot telegram](https://github.com/nlef/moonraker-telegram-bot) that allows you to regularly receive the status of the current print with an image or a short video. If the printing has failed, it is also possible to stop the printing. All this can be done outside the local network.
The user interface used is [Mainsail](https://github.com/mainsail-crew/mainsail). It's an excellent interface with a lot of features and is regularly updated.
All configuration files of the printer are available in the [Firmware](https://github.com/Graysson94/Dynasty-3D-Printer/tree/main/Firmware) folder.

## Inspirations
The creation of the Dynasty printer was inspired by this open source printers. Thanks to their creator and their community.
* Voron Trident by Voron Design [Github](https://github.com/VoronDesign/Voron-Trident)<br />
* VzBot by Vez3D [Github](https://github.com/VzBoT3D/VzBoT-Vz330)<br />
* RatRig V-Core 3 by RatRig [Github](https://github.com/Rat-Rig/V-core-3)<br />
* BLV MGN Cube by Ben Levi [Web Site](https://www.blvprojects.com/blv-mgn-cube-3d-printer)<br />

## License
The Dynasty 3D printer uses the license [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
![Dynasty_License](https://github.com/Graysson94/Dynasty-3D-Printer/blob/main/Gallery/License.PNG)

:exclamation: All 3D models created by other designers and their remixes used for this printer retain their original license. For more details, see the [3MFs STLs](https://github.com/Graysson94/Dynasty-3D-Printer/tree/main/3MFs%20STLs) folder. :exclamation: