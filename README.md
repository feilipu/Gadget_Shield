# Gadget Shield

What would you do with a single shield that has an accelerometer, speaker, microphone, infrared transmitter, infrared receiver, RGB LED, four discrete LED’s, two pushbuttons, a potentiometer, and a visible light sensor?

The Gadget Shield is an add-on (shield) compatible with the Arduino Uno, Duemilanove, Mega/Mega2560, Ruggeduino, or other compatible boards.

It extends the functionality of the microcontroller board by adding several interesting sensors and actuators. Fully assembled and ready to go, the Gadget Shield opens up a whole world of fun and learning.

All information pertaining to [the Gadget Shield has been retrieved from the Wayback Machine](https://web.archive.org/web/20121122224451/http://ruggedcircuits.com/html/gadget_shield.html). More detailed info is to be found there.
	
## Features
The Gadget Shield includes:

#### A Freescale MMA7660FC 3-axis digital accelerometer
This is a 1.5g 120 sample-per-second digital accelerometer with 6-bit resolution and neat features such as tap/shake detection and tilt/orientation detection. A copy of the [datasheet is available in the docs](https://github.com/feilipu/Gadget_Shield/blob/master/docs/MMA7660FC.pdf).

#### A high-brightness RGB LED
This module contains three independent LED’s (red, green, and blue) with independent brightness control for each color since each LED is connected to a separate microcontroller PWM output. This gives you an incredibly wide color palette to choose from. This thing is bright -- the manufacturer does not recommend looking directly at it when operating at maximum power, and we usually just run it at about 10%-20% duty cycles because that’s plenty bright.

#### A 38 kHz logic infrared detector
This module outputs a digital low signal when 38kHz-modulated infrared energy is detected, as output by most infrared remote controls. See our sample software for using this module to decode infrared remote control transmissions. Together with the infrared LED emitter, this can be also be used as a non-contact object sensor (again, we have some sample software that demonstrates this).

#### An infrared LED
This LED emits light in the 940nm wavelength range and can be used to generate infrared remote control signals. This LED is controlled by a microcontroller timer pin so it is simple to generate the 38 kHz frequencies recognized by most receivers. See our sample software for using this LED together with the IR logic detector to turn your microcontroller board into a universal remote control.

#### A speaker
Use this to generate tones, alerts, or to play simple melodies (see our sample software below). The speaker uses PWM to generate frequencies up to 3000 Hz.

#### A microphone
Use this for sound sensing or tone detection. The microphone’s raw output is amplified (gain of 100), low-pass filtered to 15.9 kHz, offset by 2.5V then connected to an A/D input pin.

#### A visible light sensor
This device outputs an analog signal inversely proportional to the intensity of visible light (more light means lower voltage). This signal is connected to an A/D input pin.

#### A thumbwheel potentiometer
The potentiometer’s rotation can be read using an A/D input pin.

#### Four LEDs
4 general-purpose LE’s are connected to four independent digital outputs (active high) for displaying status information, or perhaps a 4-bit binary value. We use these LED’s as a “VU meter” for displaying light level and sound level in our sample software below.

#### Two pushbuttons
Two general-purpose momentary-contact pushbuttons are connected to two independent digital inputs (active low).

#### Two-pin terminal block for external voltage input
For battery-powered operation or self-contained installations, it can be a pain to power an Arduino and its shields. The Gadget Shield makes this a little easier by providing a two-pin screw terminal block for easily connecting wire leads from battery packs or other power supplies. This voltage connects to the Vin node on the Arduino (through a reverse-voltage-blocking diode -- see the schematic) so is the same as plugging in a DC power jack.

#### Stacking Headers
Stacking headers let you stack another shield on top of the Gadget Shield, or you can plug wires right into each header socket for direct control over the on-board gadgets.

#### Cuttable Jumpers
What if you don’t want to use the microphone and want to reclaim analog pin A0 for something else? No problem! Every pin connection on the Gadget Shield goes through a cuttable jumper that is easily cut with a hobby knife. The Arduino pin is then disconnected from that pin’s gadget. You can then use the Arduino pin for something else by connecting to it through the stackable header. Changed your mind? Just short the jumper by soldering in a small wire, or solder in a two-pin 0.1” header and use a shunt to re-make the connection.

## Schematic

A [schematic of the AD040 Gadget Shield](https://github.com/feilipu/Gadget_Shield/blob/master/docs/ad040.pdf) can be found in the docs.

## License

This library is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.
