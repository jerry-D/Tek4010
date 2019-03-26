# Tektronix 4010 Emulator

This is a Tektronix 4010 terminal emulator for the Raspberry Pi.

It attempts to emulate the storage tube display of the 4010, including the bright drawing spot.
At the moment, it only supports persistent drawing, but there are plans to emulate the 4014 with
its ability for fading objects.

It is currently in alpha-test and updated daily.

It can be used to log into a historical Unix system such as 2.11 BSD on the PiDP11.

First, you need to login remotely into your system, for example using

	rsh -l user_name system

where "user_name" is the name of the user on the historical Unix system, and "system" is the name
of the system, for example

	rsh -l rene pdp11

If this works properly, you can use the tek4010 emulator. Call it as follows:

	tek4010 /usr/bin/rsh -l user_name system

At the moment, it only seems to work with rsh.

The following keys are not transmitted to the Unix system, but are executed locally
in the terminal emulator:

	home		clear persistent screen
	page up		clear persistent screen
	page down	clear persistent screen

These keys emulate the "page" key of the Tektronix 4010


