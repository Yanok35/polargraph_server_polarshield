polargraph_server_polarshield
=============================

Polargraph Server for ATMEGA2560 based arduino boards, primarily targetting a Polarshield v2.x motor controller.
This was the standard board for PolargraphSD machines made from 2014 to 2018.

This doesn't seem to compile in Arduino IDE v1.8.6! Why? I don't know! It works fine in 1.8.5.
It also doesn't work in the online web Arduino IDE.

** 
Please note! From mid-2018, development of new features has moved onto a ESP32-based platform. 
The codebase has changed to do this, and so v2 of this code is in a separate repo: 
https://github.com/euphy/polargraph_server_polarshield_esp32
**

A Polarshield v2.x is an add-on board for an Arduino MEGA that provides two stepper drivers, an SD card reader and 
an LCD touchscreen. The firmware may also be configured at compile time to target RAMPS, though without SD reader and touchscreen.

There is a precompiled binary hex file you can use if you don't want to compile from source.

- polargraph_server_polarshield.ino.hex is for versions of the Polarshield or PolargraphSD that shipped after August 2014.

If you have a 2.2 inch screen, then you need to compile the firmware yourself.

The program has a core part that consists of the following files that are common to all Polargraph Server versions:

- comms.ino
- configuration.ino
- eeprom.ino
- exec.ino
- penlift.ino
- pixel.ino
- util.ino

and 
- polargraph_server_polarshield.ino

which is named for the project.

The other source files include the extended functionality available on ATMEGA2560 boards
and the Polarshield.

The file called impl_ps contains implementations of a few functions, and also
contains the extended impl_executeCommand(...) which is the jumping-off point for those 
extended functions.


Written by Sandy Noble

Released under GNU License version 3.

http://www.polargraph.co.uk

https://github.com/euphy/polargraph_server_polarshield
