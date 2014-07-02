vj-uart
=======

Virtual JTAG UART for Altera Devices

Altera's Cyclone devices contain a couple of special JTAG instructions that
allow data to be passed to a "Virtual VJTAG" adapter coded into your design.

This project provides a "Virtual UART" allowing information to be easily
exchanged between a PC and the design inside the Altera chip.  This is
particularly handy for devices like the excellent Terasic DE0-Nano, that
only have one USB connection for the built-in USB Blaster.

The sample TCL script connects to the first USB Blaster device through the
Quartus STP application and listens on a TCP connection.

QUICK START:
1. Upload the bitstream to your device.  Use Quartus II or urJTag:
	urjtag ./vjtag.svf
2. Run the TCL script:
	./vjuart.tcl
3. Telnet to the listening port:
	telnet localhost 2323

If all went well, the screen should show you the alphabet, A through Z and
every character you type will be echoed back to you.
  
Copyright (C) 2014 Binary Logic (nhi.phan.logic at gmail.com).

This file is part of the Virtual JTAG UART toolkit
