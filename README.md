# Jellyfish Data Acquisition Board KiCad PCB Files
This is one of 3 repositories related to the Jellyfish Data Acquisition project. The goal is to build the hardware for a noninvasive electrode array capable of detecting neronal activity of small jellyfish, the firmware to digitize the signals and control the multiplexing of each pixel, and the software to control the system and graph the data.
| **Hardware** <br/> (You Are Here)      | Firmware      | Software |
| ------------- | ------------- | ------------- |
|<img href="https://github.com/kitsgit1/Jellyfish-Data-Acquisition-Board-KiCad" height="250"  alt="image" src="https://github.com/user-attachments/assets/67c51e2f-29f3-4307-9948-8f07744b9134" /> <br/>https://github.com/kitsgit1/Jellyfish-Data-Acquisition-Board-KiCad | <img href="https://github.com/kitsgit1/Jellyfish-Data-Acquisition-STM32" height="250" alt="image" src="https://github.com/user-attachments/assets/bd18b171-2b63-48db-b7f1-8d5697fd898b" /> <br/>https://github.com/kitsgit1/Jellyfish-Data-Acquisition-STM32 | <img height="250" href="https://github.com/kitsgit1/Jellyfish-Data-Display-GUI"  alt="image" src="https://github.com/user-attachments/assets/82673d50-fd29-4a85-90e4-c16e8167e04e" /> <br/>https://github.com/kitsgit1/Jellyfish-Data-Display-GUI |

# Hardware Documentation - Rev A
There are two boards that make up the assembly: the Electrode board and the Digitizer board.
## Jellyfish Electrode Board
The electrode board is responsible for interfacing with the jellyfish and multiplexing all pixels down to one wire using low charge-injection analog mux's. There is an optional path for a front-end buffer amplifier (non-inverting x2 gain for Rf = Rg). I/O consists of the Guard signal which drives the saltwater bath to the same potential as the op-amp reference voltage, the digital I/O to control the shift registers that select the correct pixel through setting all the multiplexers, and the single analog switched electrode signal.

## Jellyfish Digitizer Board
The digitizer board further amplifies the tiny signal from the electrode board into something the STM32's 10MHz/12-bit ADC can handle. The STM32 is also responsible for collecting, storing, and sending data to either the PC over USB or to an SD card.

Details to come...
