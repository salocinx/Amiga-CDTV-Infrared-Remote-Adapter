# Amiga-CDTV-Infrared-Remote-Adapter

The adapter is simply plugged into the mouse or joystick port and off you go. The current is drawn directly from the Amiga (approx. 15mA, the joystick port supplies up to 100mA according to Commodore) and therefore no external power supply is needed. The functionality is equivalent to conventional Amiga mice or joysticks. Switching between mouse and joystick is easy with the slide switch on the CDTV remote control.

- Demo Mouse Functionality: https://www.youtube.com/watch?v=qpLgwaQoD8I&feature=youtu.be
- Demo Joystick Functionality: https://www.youtube.com/watch?v=gpVF-gsmB1M&feature=youtu.be

Compatibility

- A500, A1000, A2000, A3000(T), A4000(T), A1200, CD32 (supported in current firmware 1.0)
- A600: problematic for mechanical reasons. Extension cable recommended (supported in current firmware 1.0)
- CD32: Control pad + Button-A works. Button-B/-C/-D follows in next firmware revision (1.1)
- C64: Follows in next but one firmware revision (1.2)
- Atari: Follows in next but one firmware revision (1.3)

I could test the range up to 8m and didn't notice any difference to 10cm. However, bright daylight can lead to functional impairments, as daylight has a high infrared component.

The hardware will probably not change. The new firmware versions can easily be reinstalled via USB (Windows or Linux computer required).

If you want to build the adapter yourself, here are all my project files, from the 3D model for the case, to the piggyback board design, the firmware written by me and CDTV infrared protocol implementation.

- CDTV Adaptor PCB (Eagle CAD): http://nicolas.baumgardt.ch/amiga/cdtv/public/CDTV_Eagle.zip
- CDTV Adaptor Part List (BOM): http://nicolas.baumgardt.ch/amiga/cdtv/public/CDTV_Partlist.zip
- CDTV Infrared Protocol Implementation (Arduino Library): http://nicolas.baumgardt.ch/amiga/cdtv/public/IRremote.zip
- CDTV Adapter Firmware 1.0.1 (Arduino Sketch): http://nicolas.baumgardt.ch/amiga/cdtv/public/CDTV_Firmware_101.zip
- 3D Housing Model for 3D Printing (STL File): http://nicolas.baumgardt.ch/amiga/cdtv/public/CDTV_Model_3D_STL.zip
- 3D Housing Model für MoI (Moments of Interest): http://nicolas.baumgardt.ch/amiga/cdtv/public/CDTV_Model_3D.zip

Here still an important info for self builders:

If you downloaded the IRremote.zip file and copied it to the /libraries folder of your ArduinoIDE installation, you will need to delete the /libraries/RobotIRremote folder as this library may cause conflicts (contains the same definitions as this library was probably originally derived from the RobotIRremote). The CDTV module I wrote for the IRremote library is not yet available in the official master branch, although I submitted it for publication a few weeks ago and the author gave the green light.

Therefore here's a copy if it should not be integrated into the IRremote library yet: http://nicolas.baumgardt.ch/amiga/cdtv/public/IRremote.zip

Here the reference to the Github Repository of the IRremote library with the hint to the installation:
https://github.com/z3t0/Arduino-IRremote

- Move the "IRremote" folder that has been extracted to your libraries directory.
- Make sure to delete Arduino_Root/libraries/RobotIRremote. Where Arduino_Root refers to the install directory of Arduino. The library RobotIRremote has similar definitions to IRremote and causes errors.
