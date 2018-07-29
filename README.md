# 3DGuardian-
3D guard protect printer from catching fire 

Auto shuts off the 3D Printer - Protects and monitor the temperatures of the hot ends and heat bed in a 3D Printer.
Description
Specs
3D Printer Guard - Pro...
Introduction

Many 3D printer firmware have some protection of thermal runaway, this feature is used to monitor the heaters and switch off the heating elements in a 3D printer down when the PID loop gets out of control. Therefore this feature should always be enabled.

In the electronics design of any 3D printer, most commonly is that switching is performed with the use of a MOSFET to the heating element. The problem here is that, when these MOSFETs fail, they fail usually in the conducting mode. This is a serious issue as if even the firmware detects something has gone wrong, the Firmware in the 3D printer will not be able to switch off the heating element. Similarly , Solid State Relays (SSRs) can have the same consequences. Thus this condition can be very dangerous if a powerful high wattage (mains-powered) heated bed is installed in a 3D printer.

The controller here can provide that extra protection against such conditions of failure by monitoring the temperature independently of two hot ends and one heat bed and has the control to enable the printer power with the use of a heavy relay.

The controller is highly configurable via two jumpers and includes a menu to adjust the hot end set temp setting.

As for sensors which can be used for this controller. any type of 100K 3950 NTC thermistor as those found on 3D printers can be used. You can also test the NTC thermistor using this controller

Design

Having spent the last 8 years with 3D printing, I always noticed the lack of protection for the electronics found in a 3d printer. Looking into this, I came up with the idea to use an existing board I developed some time ago and to use it for this project. I spent some time developing the software, and now I have a working version. The software is updatable via the connector serial, allowing for easy updates. Wifi connectivity is also onboard making it even more versatile.

-Uses 128x64 OLED Monochrome Display

-Very graphic loaded with splash screen, main screen and alarm screen

-Uses atmega328p - 16 Mhz clock

-Menu with 3 buttons - built in alarm count timer to 5 times

auto detect alarm state and present screen to reset it

Alarm reset button - Resets the alarm and resume normal mode

Detects Air quality and Smoke CO2 concentration with MQ2 sensor installed 

Supports Wifi connectivity - software can be developed to send an email or monitor it remotely.

Buzzer to alert user when thermal runaway occurs

-Relay output switches either N.O/ N.C

-Accepts 110v/220v input or 12-24v Input

Plug-able 10 pin connector on board with 10 amp contacts

LED wired with relay alerts relay is triggered !

2 Jumpers define the printer configuration

Mode	Jumper1	Jumper2	Description
0	0	0	1 hotend no heatbed
1	1	0	2 hotend no heatbed
2	0	1	1 hotend 1 heatbed
3	1	1	2 hotend 1 heatbed
Jumpers: 1= ON , 0 = OFF

Software Features

-3 channel NTC 100K - Suitable to read up to 290 Degrees

-Save set temp of each channel to eeprom instantly

-Menu allows to set temperatures of each channel

Jumper to configure 1/2 hotend and heatbed if installed

Controller check conditions and logs them to console. - serial

Full serial debug - allow to monitor status in serial port

Full graphic icons

Serial connection with ramps board to stop printer and park head * coming soon 

Smoke/ air Quality detection - with MQ2 Sensor when installed - 

Wifi connectivity ** coming soon 

---------------------------------------------------------------------------------------------------------------
Files in this folder 

User Manual and Compiled Hex files 
