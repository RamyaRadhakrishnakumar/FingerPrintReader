# FingerPrintReader
# It recognises the finger pattern and uses that pattern for security purposes.

## Table of Contents
1. [Correct Web template](#correct-web-template)
2. [Introduction](#introduction)
3. [Budget](#budget)
4. [Time Commitment](#time-commitment)
5. [Mechanical Assembly of my Fingerprint sensor](#mechanical-assembly-of-my-fingerprint-sensor)
6. [Power up](#power-up)
7. [Test Code](#test-code)

![Image of Prototype]()

### Correct Web template



### Introduction

This stackable interface board for the Broadcom development platform also known as the Raspberry Pi is of a hand solderable 
design meant to be compatible with the devices in the Humber Parts Crib which require more skills and techniques to assemble.
It has a bidirectional LED and three I2C device sockets. The bidirectional LED allows the hardware equivalent of "Hello World"
to be achieved by blinking the LED. I2C is a very common hardware peripheral bus and is designed to have an analog breakout
board, a Real Time Clock module, and an integrated environmental sensor module connected. It takes most individuals about a
week of effort to complete these build instructions directed towards technologically inclined students especially given other
commitments. Be aware that the image creation steps take at least 3 hours alone.

### Invoice/Bill:
Link--

### Budget


### Time Commitment

The time commitment was a cake walk since I created a schedule during the start of my semester.
link--
It really was one reason I organized the works properly and was able to achieve the milestones as intented.

### Mechanical Assembly of my Fingerprint sensor 

1. Connect the fingerprint to the USB to TTl convertor as follows:
(https://radiojove.gsfc.nasa.gov/telescope/soldering.htm) and can comment on them. (If you are into materials, look up tin pest and tin whiskers.)
2. This is the pinout of the USB to TTL.
![Prototype Lab](https://raw.githubusercontent.com/six0four/StudentSenseHat/master/images/IMG_20170616_184112490_HDR.jpg)
3. The pinout of the fingerprint sensor.
4. Connections using the jumper wires: 
 
 1.Connect the GN of the sensor to the GN of the TTL converter.
 
  2.Connect the RX of the sensor to the TX of the TTL converter.
 
  3.Connect the TX of the sensor to the RX of the TTL converter.
 
  4.Connect the VCC of the sensor to the VCC of the TTL converter.
 
5.Then connect the sensor through the USB port of the Raspberry Pi.

### Power up


### Test Code

1.Attached are sample files for storing a new fingerprint, reading out and deleting stored fingerprints. Let’s begin by recording a finger. Call the following:

python2 /usr/share/doc/python-fingerprint/examples/example_enroll.py

2.Put your finger on the glass surface, wait for the instruction in the terminal and remove your finger as soon as it is written there. Afterwards you have to put your finger a second time for the verification and the imprint is stored in the next number.
Let us also see whether our finger is recognized. So remove your finger from the sensor and call the following script:

python2 /usr/share/doc/python-fingerprint/examples/example_search.py

3.Put your finger on it again. If the fingerprint on the Raspberry Pi is detected, a message like this appears:

Currently stored templates: 2
Waiting for finger...
Found template at position #1
The accuracy score is: 63
SHA-2 hash of template: 3aa1b01149abf0a7ad0d7803eaba65c22ba084009700c3c7f5f4ecc38f020851
