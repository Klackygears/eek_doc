# eek

![eek](https://i.imgur.com/34O3xKW.jpg)

The eek! Is a 36 key per key RGB keyboard with a 90 degree split layout suited for travel and typing close to the body. It uses a Pro Micro or an Elite C and can be soldered low profile using castilated pads. The PCB can be flipped so that the silk is on top and the USB plugin can face to the right or left by uncommenting "OPT_DEFS += -DFLIPPED" in the rules.mk file. The keyboard is compatible with MX, Alps, and Choc style switches. It can use SMD or through hole diodes. The per key RGB LEDs used in the build are the SK6812 Mini E (these can also be flipped). The eek! can be used without a case if you choose for a very low profile keyboard. 


In the Case_Files folder, you will find the .svg and .dxf files to make your own case if you like.

In the QMK_Files folder, I've placed the needed qmk keyboard folder in case you would like to program the keyboard before the firmware is pulled into the main branch. Alternatively, here is a link to my eek! branch [eek! QMK Firmware branch](https://github.com/Klackygears/qmk_firmware/tree/eek_qmk). Both have a basic keymap and a LED tesk keymap to make it easier to test your led soldering.


## Assembling the eek!

The eek! follows the normal rules when assembling the board. Below is an example of how the diodes, LEDs, and MX switches should be soldered. Keep in mind that if you flip the board to show the bat and eek! silk up, these same rules apply. 

![eek_bat](https://i.imgur.com/YrOqmft.jpeg)


The footprints for the diodes have a small arrow indicating whitch direction the black line (or white line with SMD diodes).

![diode_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_diode.jpg)

The LED order is below. Like Christmas lights, if you have a problem with one of the LEDs all of the LEDs after will not work.

![LED_order](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_diode.jpg)


The SK6812 MINI E (be sure to get the **"E"** type) have one leg that has a clipped angle. That angled leg should be placed on the pad with the outline.

![LED_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_LED.jpg)


The eek! is compatible with MX, ALPs, and Choc style switches. In the first image below, be careful not to bridge solder across the red lines. Depending on your configuration, you may connect the column and rows so that the switch always appears to be pressed. This will cause strange problems. In the second image below, the colored dots represent the switch legs in the footprint: Red for MX, Green for ALPs, Blue for Choc. 

1)
![switch_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_switch.jpg)

2)
![switchtypes_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_switch_types.jpg)


The Pro Micro (or clone) should be soldered to the pcb on the side with the gear logo as seen in the picture below. If you are using a variant with castilated holes, the pads on eek! support soldering the Pro Micro on that way for a low profile build. **_Regardless if you decide to have the pcb flipped or not, the pro micro should be installed the same way._** 

**I recommend flashing firmware on the pro micro before soldering to make sure that it's working properly.**

![ProMicro_orientation](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/ProMicro_placement2.jpg)


## Flashing the eek!

Once you have your build environment set up using the guide in the **[QMK Documentation](https://docs.qmk.fm/)** I recommend flashing the eek! with the default keymap or the ledtest keymap to make sure that everything is soldered correctly. QMK firmware github is [here](https://github.com/qmk/qmk_firmware).

If you made the eek! with the bat silk side down use the command:

``make eek:default``

If you made the eek! with the bat silk side up use the command:

``make eek/silk_up:default``


Disclaimer: Though it may be tempting, eek! is not a snack.
