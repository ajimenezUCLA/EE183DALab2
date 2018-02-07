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
## Setup
### Instrument 1: Chopstick Drumstick
The drumstick instrument utilizes an ESP8266, a motor control board, a servo, and lastly a chopstick. This ESP8266 acted as the master in our jam band. It relayed information via two serial connections to the other ESP8266. The servo was connected to D0 on the master controller. This component also served as the host for the website.
![drumstick](https://images-na.ssl-images-amazon.com/images/I/41-aA8t56uL._SX342_.jpg "servo")
### Instrument 2: Buzzer
The buzzer was a very useful instrument as the arduino code allowed us to play various notes with it. This instrument was connected to a reciever ESP8266. This ESP8266 awaited on commands from the master ESP8266 which would allow it to determine the song and tempo.
![buzzer](http://www.futurlec.com/Pictures/3VPIEZOPCB.jpg "buzzer")

## Steps
### Step 1: ESP8266-E12 & MCU
The ESP8266 is a microcontroller much like the popular Arduino, except it has built in wifi.
Set up instructions can be found here.
http://www.instructables.com/id/Programming-the-ESP8266-12E-using-Arduino-software/ 

#### Pinout
![MC1](http://amazingrobots.net/wp-content/uploads/2016/06/nodemcu_pinout.png "ESP 8266")
![MC2](http://amazingrobots.net/wp-content/uploads/2016/06/motor_shield_diagram.jpg "MCU")

### Step 2: Theory & Data Collection
![sensor1](https://github.com/waterbottels/EE183DALab2/blob/master/component1.png "sensor 1")
![sensor2](https://github.com/waterbottels/EE183DALab2/blob/master/component2.png "sensor 2")
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/sensors1.png "M")
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/sensors2.png "M")
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/sensors3.png "M")
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/sensors4.png "M")
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/sensors5.png "M")
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/sensors6.png "M")

### Step 3: Logic Design & Execution
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/mechanics.png "Mechanical Drawing")

![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/schematic.png "Schematics")
### Step 4: Code
The code can be found here:
https://github.com/ckwojai/EE183_JamBand/tree/master/code

## Multi-Robot Collaboration
Essentially, one acts as a sender (master) and the other acts as a reciever (slave). Serial communication basically means the sender will do a Serial.Print('R') *(R stands for ready)* before executing any instrument playing code.
The receiver will check Serial.available() and the signal from the Serial buffer. If it gets an R, it sets this alue as true which iniates the instrument playing code. This is true for the tempo and song selection.
## Website
![alt text](https://github.com/waterbottels/EE183DALab2/blob/master/website2.png "Website")


## Demonstrations
