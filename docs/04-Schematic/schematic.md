---
title: Schematic
---

## Overview

The power distribution board for a multi-board robotics project. It takes 9V from a barrel jack through a fuse and reverse-protection diode, then splits the power into three outputs:

5 V logic from a linear regulator, for the microcontroller and other boards’ electronics
5 V motor supply (up to 3 A) from a buck converter, for the motor board
Raw input voltage passed through to any board that needs it
A PIC18F57Q43 Curiosity Nano runs the board. A current-sense circuit measures motor current through a shunt resistor and reads it on an ADC pin. The board also has a UART ribbon connector, spare GPIO headers, test points, a power LED, two debug LEDs, and a debounced switch.


![schematic](JB_Schematic.png){style width:"350" height:"300;"}
**Figure:** Here is my Schematic.



