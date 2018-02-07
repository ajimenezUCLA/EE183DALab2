# EE183DA - Lab 2

## Introduction
Our goal was to build a musical "jam band" driven by two ESP8266 microcontrollers, utilizing sensors and actuators. We have an autonomous mode which gives the user an option between two songs, *Row Row Your Boat* and *Twinkle Twinkle*. The user can also decide the tempo of the song in the autonomous mode. The Human controlled mode allows a user to change the songs using a touch sensor and vary the speed of the song with an ultrasonic sensor. The user is given instructions on the website on how to modulate the jam band.

## Bill of Materials
| **QTY** | **Part Number**   | **Part Name**                | **Description**                        | **Spec Sheet**                                                                                                                               |
|-----|---------------|--------------------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | FS90          | Micro Servo 9g           | Small blue, used for tapping       | http://www.mantech.co.za/Datasheets/Products/FITEC_FS90.pdf                                                                              |
| 1   | Accessory-187 | Jog Type Touch Sensor    | Square blue, 3 prong. Senses touch | https://www.amazon.com/Sensor-Capacitive-Arduino-Atomic-Market/dp/B00WH7O00U                                                             |
| 1   | HC - SR04     | Ultrasonic Raning Module | looks like robot eyes              | http://www.micropik.com/PDF/HCSR04.pdf                                                                                                   |
| 2   | 12E           | ESP 8266MOD              | Microcontroller                    | http://amazingrobots.net/2017-2/resources/nodemcu_pinout/                                                                                |
| 1   | 571CK         | Chop Stick               | A wooden Chopstick                 | https://docs.google.com/viewer?url=patentimages.storage.googleapis.com/pdfs/US20090026782.pdf                                            |
| 1   | MCBB400       | Breadboard               | For holding components             | https://www.melopero.com/datasheets/Breadboard.pdf                                                                                       |
| 1   | 1956725       | PCB Mini Buzzer          | a small black speaker              | https://www.jameco.com/z/SV8-Velleman-Audio-Indicator-and-Alerts-Buzzer-8mA-12-Volt-Solder-Through-Hole_1956725.html                     |
| 1   | RS002C        | Wire Jumper Kit          | Wires for Connecting components    | https://www.jameco.com/z/RS002C-Dagu-HiTech-Electronic-Wire-Jumper-Kit-140-Pieces-100-Male-Cables-40-Female-Cables-5-Colors_2150467.html |
| 1   | OOBG          | 330 ohm + 5% resistor    | a resistor                         | https://www.sparkfun.com/products/11507                                                                                                  |
| 1   | 12E           | Motor Shield             | Housing for ESP 8266               | https://hackaday.io/project/8856-incubator-controller/log/29291-node-mcu-motor-shield                                                    |
| 2   | LP-503562     | 3.7v Battery             | Powers the robot                   | https://www.adafruit.com/product/258                                                                                                     |
## Schematics
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/mechanics.png "Mechanical Drawing")

![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/schematic.png "Schematics")

## Setup
### Instrument 1: Chopstick Drumstick
The buzzer instrument utilizes an ESP8266, a motor control board, a servo, and lastly a chopstick. This ESP8266 acted as the master in our jam band. It relayed information via two serial connections to the other ESP8266. The servo was connected to D0 on the master controller.
### Instrument 2: Buzzer


## Multi-Robot COllaboration

## Website
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/website.png "Website")


## Demonstrations
