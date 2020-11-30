# eek

![eek](https://i.imgur.com/34O3xKW.jpg)

The eek! Is a 36 key per key RGB keyboard with a 90 degree split layout suited for travel and typing close to the body. It uses a Pro Micro or an Elite C and can be soldered low profile using castilated pads. The PCB can be flipped so that the silk is on top and the USB plugin can face to the right or left by uncommenting "OPT_DEFS += -DFLIPPED" in the rules.mk file. The keyboard is compatible with MX, Alps, and Choc style switches. It can use SMD or through hole diodes. The per key RGB LEDs used in the build are the SK6812 Mini E (these can also be flipped). The eek! can be used without a case if you choose for a very low profile keyboard. 

![eek_bat](https://i.imgur.com/YrOqmft.jpeg)

In the Case_Files folder, you will find the .svg and .dxf files to make your own case if you like.

In the QMK_Files folder, I've placed the needed qmk keyboard folder in case you would like to program the keyboard before the firmware is pulled into the main branch. Alternatively, here is a link to my eek! branch [eek! QMK Firmware branch](https://github.com/Klackygears/qmk_firmware/tree/eek_qmk). Both have a basic keymap and a LED tesk keymap to make it easier to test your led soldering.


Assembling the eek!

The eek! follows the normal rules when assembling the board. The footprints for the diodes have a small arrow indicating whitch direction the black line (or white line with SMD diodes).
![diode_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_diode.jpg)

The SK6812 MINI E (be sure to get the "E" type) have one leg that has a clipped angle. That angled leg should be placed on the pad with the outline.
![LED_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_LED.jpg)

The eek! is compatible with MX, ALPs, and Choc style switches. In the first image below, be careful not to bridge solder across the red lines. Depending on your configuration, you may connect the column and rows so that the switch always appears to be pressed. This will cause strange problems. In the second image below, the colored dots represent the switch legs in the footprint: Red for MX, Green for ALPs, Blue for Choc. 
1)
![switch_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_switch.jpg)
2)
![switchtypes_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_switch.jpg)
Disclaimer: Though it may be tempting, eek! is not a snack.
