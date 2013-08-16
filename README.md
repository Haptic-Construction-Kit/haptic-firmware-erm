haptic-firmware-erm
===================

Haptic Firmware for ERM tactors

INTRODUCTION

This directory contains the firmware code for the erm tactor type. The ATtiny48 code was developed under Linux using the AVR GCC toolchain (avr-gcc, avr-libc, avrdude, and so forth) and may make use of some constructs specific to that toolchain. 

BUILDING THE DOCUMENTATION

Install Doxygen and Graphviz, then run the builddoc script in this directory.
HTML documentation will appear in doc/funnel for the Funnel I/O side and
doc/tiny for the Haptic Tactor side. This is primarily useful to get call graphs
and caller graphs for all the functions in the code.

BUILDING THE TACTOR CODE

The Tactor is programmed entirely in AVR C Code, including nothing from Arduino.
Install the AVR toolchain and related tools: avr-gcc, avr-libc, avrdude, and
so forth. Then take a look at the build, dump, and avrdude scripts in this
directory to see which commands to use to build the code and program the
ATtiny88. The AVRISPmkII USB in-system programmer was used during development;
the arguments to avrdude (as specified in the avrdude script in this
directory) may need to be modified if a different programmer is to be used.
See the avrdude documentation for details.
ex:
./build -DDEFAULT_TWI_ADDRESS=34


