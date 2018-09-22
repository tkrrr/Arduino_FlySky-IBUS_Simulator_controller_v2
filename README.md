# Arduino_FlySky-IBUS_Simulator_controller_v2
This project uses an Arduino Micro to decode an IBUS signal and emulate a joystick device for use with quadcopter simulators.
The project is based on: 
https://github.com/Slattsveen/Arduino_FlySky-IBUS_Simulator_controller
https://github.com/povlhp/iBus2PPM

Following changes were made:
- uses hardware serial
- changed the joystick type as the one used in the original project didn´t work on all systems
- changed the way ibus is read, now reading 10 channels and using checksum (code from IBus2PPM project)

Builds on the following libraries, they are needed for my sketch to work:
- FlySky Ibus decoder by aanon4: https://github.com/aanon4/FlySkyIBus
- Joystick library by Matthew Heironimus  - http://mheironimus.blogspot.no/2016/11/arduino-joystick-library-version-20.html 
                                          - https://github.com/MHeironimus/ArduinoJoystickLibrary/tree/version-2.0

Components:
- 1 Arduino micro (should work directly on a Leonardo as well, can probably be adapted to other models also)
- 1 FlySky IBUS receiver (tested with the FlySky X6B)
- FlySky radio controller (I use the FS-i6)

Setting up: Use hardware Serial to read the incoming IBUS channel: RX=IBUS,VCC=5V,GND=GND

Disclaimer: I share this code with the community, I will not be developing it further unless I wish to change something for myself. Feel free to copy and modify as you wish.
