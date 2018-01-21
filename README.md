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

E-money transfer is a convenient way to send, receive or pay bills in store using a simple QR code generator. I’m using a finger print sensor in collaboration with the software app. The sensor is used as a safety measure to prevent loss of information. In order to access your account you need to login using your login credentials including the finger print pattern that is registered along with your bank account in the E-money application. Basically the finger print lets you enroll, delete, search or generate a picture of your finger. To this I used a raspberry pi. 


### Invoice/Bill:
Link--

### Budget

The Fingerprint sensor(751) costed me $64.00. 
The Raspberry pi costed me $99.99.
The USB to TTL convertor costed me $6.99.
The Jumper wires costed me $5.99

### Time Commitment

The time commitment was a cake walk since I created a schedule during the start of my semester.
link--
It really was one reason I organized the works properly and was able to achieve the milestones as intented.
Setting up the hardware must take around 20 minutes and testing it should be around 10 minutes.

### Mechanical Assembly of my Fingerprint sensor 

1. Connect the fingerprint to the USB to TTl convertor as follows:

2. This is the pinout of the USB to TTL.

3. The pinout of the fingerprint sensor.

4. Connections using the jumper wires: 
 
 1.Connect the GN of the sensor to the GN of the TTL converter.
 
  2.Connect the RX of the sensor to the TX of the TTL converter.
 
  3.Connect the TX of the sensor to the RX of the TTL converter.
 
  4.Connect the VCC of the sensor to the VCC of the TTL converter.
 
5.Then connect the sensor through the USB port of the Raspberry Pi.

### Power up
So once I assembled the hardware part, I then connected my mouse and keyboard along with the charger cable to my pi and then turned it ON. Also I need not connect the ethernet cable since I already configured the pi to connect it to the Wi-Fi. I was able to see the sensor light up. You will be able to achieve this if your hardware connection is perfect.

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
