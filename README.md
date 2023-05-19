# ATMAE Robotics Competition
Code for manual and autonomous navigation of robot. Our entry was awarded **2nd prize** at the 2015 ATMAE Robotics Conference, Pittsburgh, PA.

## About the competition
https://www.atmae.org/page/RoboticsCompetition

## Description

<p align="center">
  <img src="Planning/ATMAE 2015-16.png" alt="Demo" width="80%" height="80%"/>
</p>

The robot is controlled by two python scripts. The first of the scripts runs on a computer. The second script runs on a Raspberry Pi. The computer’s python script handles operator input through the use of a wireless Xbox 360 controller. The computer sends data via TCP to the Raspberry Pi. This is accomplished by the connection of both devices to the same network, in this case a personal router. The Raspberry Pi receives the data sent by the computer and processes it in order to control the robot’s hardware.

Each motor and each servo is controlled by pulse width modulation (PWM). The DC motors have an intermediary motor controller to process the PWM signals. The servos are directly controlled with PWM by design. PWM output on the Raspberry Pi is possible through the addition of a PWM controller, which interfaces with the Raspberry Pi via I2C. I2C also enables the use of an analog-to-digital converter (ADC). The ADC is used to convert the signals from analog reflectance sensors to digital data that can be read by the Raspberry Pi. All devices are run on 5V logic.