# UNM-CS499-f23LMS-hw2-output-can-bus

Assignment 2 – Data Output Demonstration

# Discrete Outputs & Binary Address Generation

Objective: Use the Serial Monitor (Terminal) to input data, create a program to write a binary pattern to a group of four discrete outputs. 

1. Configure pins 34, 35, 36 and 37  as outputs which are connected to LEDs on the breadboard.
2. Input a number from 0 to 15 on the Serial Monitor and convert it to the 4-bit binary value. i.e. 5 => 0x0101b
3. Display the binary value on the breadboard LEDS and verify the correct pattern. pin 34 = Address 3, pin 35 = Address 2, pin 36 = Address 1, pin 37=Address 0


# CAN Bus Output Message 


Objective: Generate a CAN Bus test message and output it to the CAN Bus at a 1Hz rate using the ACAN_T4 library.

(Target hardware is TBD.  The LMS2023 BTMS boards have transceiver chip installed so they are they can be used with a fabricated CAN Bus test cable)

Controller Area Network (CAN) is the most common serial communication network used for automotive, marine and off-road equipment applications. For a complete description, see https://en.wikipedia.org/wiki/CAN_busLinks to an external site. 

1. The ACAN_T4 library must be downloaded from GitHub https://github.com/pierremolinaro/acan-t4Links to an external site.  Be sure to download the associated readme and User Manual for this library

2. Install the library into the Teensyduino IDE using the Sketch/Include Library/Add .ZIP Library feature

3. Create a sketch to generate a CAN bus message that emulates the OrionBMS Thermistor Expansion Module. See [thermistor_module_canbus.pdf](thermistor_module_canbus.pdf) for a description of the OrionBMS message format

4. Configure Pin 0 for RX1 and Pin1 as TX1

5. Testing the sketch will require use of a Teensy with a CAN Bus Transceiver Integrated Circuit (IC) connected to Pin 0 and Pin 1.  The Transceiver IC will be connected to a Microchip CAN Bus Analyzer. Use of the CAN Bus Analyzer requires installation of the associated software on a laptop. The laptop is connected to the Analyzer via USB.

6. Load your sketch into the Teensy on the BTMS circuit board.

7. Disconnect the BTMS board from your laptop. Connect the BTMS board to the CAN Bus Analyzer.  Power the board using an external power supply.

8. Connect the CAN Bus Analyzer to your laptop and start the CAN Bus Analyzer software

9. Use the CAN Bus Analyzer to verify the message is correct
