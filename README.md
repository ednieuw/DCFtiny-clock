# DCF77 HC-12 Bluetooth transceiver clock

<p><img alt="DCFklok" height="450" src="DCF77transceiverclock.jpg" /></p>
This clock decodes the DCF77-signal, displays the received 
bits in WS2812 RGB rings and sends the time as a string into the ether with a HC-12 433MHz Wireless Serial Transceiver.</br>
The software makes use of an algorithm that collects the readings without using interrupts.</br>
In this program the processor is able to collect, in it spare time, over 30,000 per second of 0 or 1 readings.</br>
Therefore no delays() can be used. The program demonstrates a method to avoid delays. </br>
An advantage of this method is it smoothens spikes in the signal.</br>
The routine is smaller than the DCF library and can be easily debugged.</br>
The efficiency is comparable with the DCF77 library of Thijs Ellenbaas.
With good reception both methods decode over 99%.</br>
The interupt and non-interupt methods are used in this program and increases the efficiency even further.</br>
By turning on and off the #defines in the program one or both methods can be used
The DCF-noninterupt algorithm was developed to drive the LEDs of the clock. The clock 
contains three rings of 8, 24 and 60 LEDs.</br>
The outer ring displays the received bits per minute. blue = 0 and red = 1.
The middle ring display the signal efficiency per hour and the current hour with 
a white LED.</br>
The inner ring displays various parameters.</br>
On top of the clock is a TM1637 or HT16K33 display to show the current time.<br>
A MAX7219 display is used to show the pulsewidth in msec, the time as it is decoded by the algorithm<br>
and the decoding efficiency in time as a percentage.</br>
The time is transmitted in the air with a HC-12 transceiver.</br>
With a Bluetooth module the clock can be operated with a phone.</br>
More info about clocks and DCF77 here:</br>
<a href="https://ednieuw.home.xs4all.nl/Woordklok/index.html">
https://ednieuw.home.xs4all.nl/Woordklok/index.html</a></p>
