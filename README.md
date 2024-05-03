[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/kzkUPShx)
# a14g-final-submission

    * Team Number: 26
    * Team Name: Circuit Crusaders
    * Team Members: Saurabh Parulekar, Binh Nguyen
    * Github Repository URL: https://github.com/ese5160/a14g-final-submission-t26-circuit-crusaders
    * Description of test hardware: 
      1. HP Pavilion Windows Gaming laptop, 15" 8GB i5
      2. Apple M2 Pro - Macbook 

## 1. Video Presentation

## 2. Project Summary

## 3. Hardware & Software Requirements

### Hardware Requirements

- Directional Haptic Vibration Notification System:

  - HRS 01- We constructed a 3d Model that went around the helmet from the back; at either end of the semi-circular housing, we mounted a Haptic Motor. Individual haptic motor drivers with common I2C buses controlled these motors. The devices were selected using an enable line(**Met**).

![Haptic Motors](https://github.com/ese5160/a14g-final-submission-t26-circuit-crusaders/blob/main/images/Haptic%20Motors.jpg)

- Blind Spot Monitoring System:

  - HRS 02- Designed mounting for Sharp IR sensors, which were polled when a turn signal was active. The IR sensor used had an analog output, which was converted to a digital signal using Opam as a comparator, and the distance for detection was set using potentiometers(**Met**).

![IR sensor]()

- Accelerometer System:

  - HRS 03- An On-Board accelerometer was included, which polled all the axes. The z-axis data was used to detect the deceleration of the rider, while other axes were used to detect theft in lock mode and fun mode to change the LED strip light(**Met**).


- Bluetooth Module:

  - HRS 04- We dropped installation of the Bluetooth module due to the limited time and effort required for developing mutex-protected UART communication and the requirement for a Mobile App(**Not Met**).

- Wifi Module:

  - HRS 05- The wifi module, integrated in the SAMW25, was used to connect to the MQTT hosted on Azure VM and communicate with the Node-Red Dashboard(**Met**).

- Indicaion LED System:

  - HRS 06- We decided to use a single LED strip and control the LEDs on the strip to indicate Left and right turns and brake(**Met**).

![LED Strip]()

### Software Requirements

- Directional Haptic Vibration Notification System:

  - SRS 01 - The software shall control the vibration motor via a motor driver controlled over I2C protocol to vary intensity based on distance from a turn and navigational data(**Met**)

  - SRS 02 - The software shall enable the appropriate vibration motor(left or right) based on directions received. It shall have different vibration patterns and intensity based on the type of turn and distance from a turn(**Met**)

- Blind Spot Monitoring System:

  - SRS 03 - The software shall start recording obstacles from the Obstacle sensors when turn signals are active(**Met**).

  - SRS 04 - The software shall also indicate to the user via vibration motors if obstacles are present(**Met**).

- Accelerometer System:

  - SRS 05 - The accelerometer shall continuously read all axes every 500ms with a resolution of 16 bits(**Met**).

  - SRS 06 - The accelerometer shall detect if the rider is stationary or in motion(**Not Met**).

        - It was not possible to do the above; we need a fixed reference to calculate the velocity of the rider.

  - SRS 07 - The accelerometer shall be used to detect a crash and raise an alert(**Not Met**).

    - We did not implement this feature in the final demo

  - SRS 08 - The accelerometer shall detect unusual motion when the helmet is in lock mode(**Met**).

- Bluetooth Module:

  - SRS 09 - The software shall manage the Bluetooth module to establish an effective and reliable wireless connection between the helmet and a smartphone for data transmission for receiving navigational data only(**Not Met**).

- Wifi Module:

  - SRS 10 - The software shall manage the Atmel® SmartConnect ATWINC1500 wifi module to enable wireless internet connectivity for IoT applications in the helmet(**Met**).

- Indication LED System:

  - SRS 11 - The system shall turn left and right LED strips to blink orange during a respective turn signal(**Met**).

  - SRS 12 - The system shall blink the brake LED strip when the rider is stationary and turn solid when in motion. stationary and motion states will be determined via the accelerometer(**Met**).

    - We detected deceleration instead of stopping



## 4. Project Photos & Screenshots
