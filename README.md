
Basic I/O pin usage:
====================

D0: Serial RXD for PC interface as well as XBee module.
D1: Serial TXD for PC interface as well as XBee module.

D2: Strobe for LCD display shift register (standard HD44780 alphanumeric display connected via 74HC4094 8-bit latch.)
D3: LCD shift register data, (Digital output)
D4: LCD shift register clock. (Digital output)

D5: LCD display backlight. (Digital output, PWM OK)

D6: Rotary encoder digital Gray-code channel "A". (Digital input)
D7: Rotary encoder digital Gray-code channel "B". (Digital input)
D8: Rotary encoder "button". (Digital input)

D9: RGB LED, red channel (Digital output, PWM OK)
D10: RGB LED, green channel (Digital output, PWM OK)
D11: RGB LED, blue channel (Digital output, PWM OK)

D12: Open-collector transistor output 1. (Digital output)
D13: Open-collector transistor output 2. (Digital output)

A0: Temperature sensor (Analog input, MCP9701A)
A1: Light sensor (Analog input, TPS852)

A2: Touchscreen pin 1. (Standard 4-wire Nintendo-style touchscreen.)
A3: Touchscreen pin 2.
A4: Touchscreen pin 3.
A5: Touchscreen pin 4.

Power supplies:
===============

Power can be supplied over the USB port, using either a PC or a 5V plugpack with USB connector.
If power is supplied via USB, the USB power jumper must be closed. Power from the USB port can be disconnected by removing the jumper.

Power can also be supplied via batteries.

This power input is stepped up to 5 volts from a lower voltage input.

Because a boost converter cannot regulate the voltage when the voltage supplied is higher than the intended output voltage, the output voltage must not exceed 5 volts.

The acceptable input voltage range is about 2.4 - 5 V. INPUT VOLTAGE MUST NEVER BE IN EXCESS OF 5 VOLTS.

Here are some examples of possible battery configurations you might use:

2 x AA cells in series - 3 V if 1.5V alkaline cells are used, or about 2.4 V if 1.2V NiMH cells are used.

2 x C cells or D cells in series can be used; these will have higher charge capacity, meaning longer battery life.

3 x AA cells in series (or C or D cells, etc.) This will give 4.5 V with 1.5 V alkalines, or 3.6 V with 1.2 V NiMH cells.
This increased voltage with 3 cells will mean that the boost converter will draw less current, meaning longer battery life.

1 x single-cell lithium-ion or lithium-ion-polymer (with a cell voltage of 3.6 V or so) can also be used, giving high energy density and long life if a large cell is used.

There is no integrated battery charging. Batteries must be disconnected and charged externally.

Arduino shield usage:
=====================

There are standard Arduino-shield-footprint pads on the PCB. These can be used to attach a standard Arduino shield.

However, most Arduino shield devices probably won't work because all the AVR pins are already used by the on-board hardware devices.
Furthermore, you won't be able to use the LCD at the same time as you've got a shield on the top of the board.

You could attach a "back-to-front" Arduino shield, with headers on the top of the board, to the back of the Pebble board.
Or, alternatively, you might take a prototyping shield such as those from Freetronics and flip it over, put some components on the back of the board, then attach headers to
the top side and put the shield on the back of the pebble board.

Female headers for the Arduino shield should be attached to the bottom of the pebble board.

Basically, there is no officially supported Arduino shield configuration that can be used with the pebble... it provides a flexible breakout for the microcontroller pins
which advanced users might want to experiment with.



















































