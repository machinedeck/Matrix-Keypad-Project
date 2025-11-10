# Matrix Keypad Project
_Last Update: November 11, 2025_

## Background
This is a simple project I started when I saw a matrix keypad in my Arduino Kit. The initial idea I have is to build an "instrument" where pressing the keys creates sound, and both the RGB LED module and matrix tube would show visualizations. It was a fancy idea, but far from completion if I could not even set up the keypad. I did not also know where the breadboard was; however, I was really curious as to how it would be done.

The solution I came up with was to involve some circuit simulation. Once I would have the simulation, I could use this information to create signals that I could feed to Arduino, as if I were doing a test bench for VHDL.
<p align = "center"><img src = "Images/matrix_keypad.png"></p>
<p align = "center"><b>Figure 1.</b> Illustration of the matrix keypad with the connections I adopted from [<a href = "https://www.circuitbasics.com/how-to-set-up-a-keypad-on-an-arduino/">1</a>].</p>

## Introduction
I have a 4x4 keypad with 8 pins as illustrated in Fig. 1, which I do not know the specifications or type. My Arduino kit only shows "Key Board 1PCS". Since I wanted to test it but I did not have the necessary electronic parts for connections, I decided to perform simulations first. I also though that performing simulations and test bench could save me time for developing the codes later as I would just have to connect everything and see if it works.

My assumption is that the keypad is a matrix of switches, and the connections I have followed is given below:
<p align = "center"><img src = Images/switches.png></p>
<p align = "center"><b>Figure 2.</b> Circuit schematic of the keypad switches arranged in a 4x4 matrix. The blue lines correspond to rows while the red ones correpond to columns (Adopted from [<a href = "https://circuitdigest.com/microcontroller-projects/interface-4x4-membrane-keypad-with-arduino">1</a>]).</p>

I saw this "1-Wire Keypad Interface With Arduino" from [2](https://www.electronicwings.com/arduino/4x4-keypad-interfacing-with-arduino-uno), and I wanted to challenge myself to design a circuit that determines which key is pressed only from a single output. This is what I ended up with:
<p align = "center"><img src = "Images/circuit.png"></p>
<p><b>Figure 3.</b> Schematic of the single output keypad circuit. The row connections are in series, and so are the columns, with the output measured at node C1.</p>


# References
[1] [https://www.circuitbasics.com/how-to-set-up-a-keypad-on-an-arduino/](https://www.circuitbasics.com/how-to-set-up-a-keypad-on-an-arduino/).

[2] [https://circuitdigest.com/microcontroller-projects/interface-4x4-membrane-keypad-with-arduino](https://circuitdigest.com/microcontroller-projects/interface-4x4-membrane-keypad-with-arduino).

[3] [https://www.electronicwings.com/arduino/4x4-keypad-interfacing-with-arduino-uno](https://www.electronicwings.com/arduino/4x4-keypad-interfacing-with-arduino-uno).
