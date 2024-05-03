[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/kzkUPShx)
# a14g-final-submission

    * Team Number: 
    * Team Name: 
    * Team Members: 
    * Github Repository URL: 
    * Description of test hardware: (development boards, sensors, actuators, laptop + OS, etc) 

## 1. Video Presentation

## 2. Project Summary

## 3. Hardware & Software Requirements

### Hardware Requirements

Directional Haptic Vibration Notification System: *Met*
We constructed a 3d Model which went around the helmet from the back, at either end of the semi-circular housing we mounted an Haptic Motor. these motors were controlled by individual haptic motor drivers with common I2C bus, the devices were selected using an enable line.


Blind Spot Monitoring System:
HRS 02 - Dual IR distance sensors to detect objects in the vehicle's blind spots, with a maximum detection range of 1 meter. IR distance sensor's analog output shall be given to an OPAM which will generate a digital signal depending on the distance selected
Accelerometer System:
HRS 03 - 3-Axis Accelerometer shall be used to detect rider motion. It shall communicate with the microcontroller over SPI/I2C.
Bluetooth Module:
HRS 04 - The system shall use smartphone Bluetooth for data transmission and a Bluetooth module on our board for reception. The Bluetooth module shall communicate with the microcontroller over UART.
Wifi Module:
HRS 05 - This system shall incorporate the Atmel® SmartConnect ATWINC1500, which shall be used for uploading and downloading vitals and commands from a cloud dashboard respectively. it shall communicate with the microcontroller through SPI.
Indication LED System:
HRS 06 - The system shall include left and right turn LED indicators and a brake light LED strip. it shall communicate with the microcontroller via I2C. Left, Right and Brake LED strips shall be daisy-chained together and share the same I2C bus.

## 4. Project Photos & Screenshots
