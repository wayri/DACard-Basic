# DACard-Basic
This is a custom data acquisition card based on the STM32F103C8Tx platform.
This board has some necessary front-end electronics and the interfacing software. The board has the following features

Here is a pic of the board running some hardware diagnostics
![DACard-BASIC Gain Diagnostic](https://raw.githubusercontent.com/wayri/DACard-Basic/master/dacard-diagnostic.jpeg)

The red LEDs are used to indicate hardware gain selection setting (both should be off - Thus a good test)

## Features
- STM32F103C8Tx microcontroller (Blue-Pill) running at 72MHz
- 4 DC ADC channels
- 1 low voltage AC signal sensing channel (SIGNAL // not power)
- 1 configurable level crossing detector
- 10 GPIO digital pins
- 2 High power shared pins (shared 2x digital GPIO pins)
- On board current sensor (shared DC ADC pin)
- On board voltage sensor (shared DC ADC pin)
- DIP6 shared|software configured digital header [can be programmed to test logic and stuff]
- 3 high speed PWM pins with adjustable dead time insertion
- 3 complimentary PWM pins


All ADCs run at 12MHz[APB2] - The sampling is set to attain a good 4 Msps overall. which is shared between 4 DC channels on ADC1 [~ 1Msps each] and between 2 channels on ADC2 for AC and crossing detection [~2Msps].

### ! The software for the setup is currently in Gamma|closed-source
 > Once it becomes stable enough it will be released under an appropriate licence

## The repository
This repository contains the pictures of the prototype hardware | design and under test.
The code is not currently included
