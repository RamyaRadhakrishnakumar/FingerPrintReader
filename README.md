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



### Correct Web template

I created a web template https://github.com/RamyaRadhakrishnakumar/FingerPrintReader/ for this particular project as per the course requirement. I update my webpage on a weekly basis as I go forward in building my project. You can see that I have uploaded pictures and files involving informations of my project in the above entioned webpage.

### Introduction

E-money transfer is a convenient way to send, receive or pay bills in store using a simple QR code generator. I’m using a finger print sensor in collaboration with the software app. The sensor is used as a safety measure to prevent loss of information. In order to access your account you need to login using your login credentials including the finger print pattern that is registered along with your bank account in the E-money application. Basically the finger print lets you enroll, delete, search or generate a picture of your finger. To this I used a raspberry pi. 

![System diagram]()

### Invoice/Bill:

I ordered the sensor from Adafruit website. I ordered my pi, USB to TTL and jumper wires from Amazon. It roughly took a week to reach.
![Invoice]()

### Budget

The Fingerprint sensor(751) costed me $64.00. 
The Raspberry pi costed me $99.99.
The USB to TTL convertor costed me $6.99.
The Jumper wires costed me $5.99

### Time Commitment

The time commitment was a cake walk since I created a schedule during the start of my semester.
link--
It really was one reason I organized the works properly and was able to achieve the milestones as intented.
Setting up the hardware must take around 20 minutes provided if you have the equipments and have previous knowledge of the hardware. I took roughly 1 week to set it up. I used python code to make the sensor work. The testing should take around 10 minutes, but I actually took time to read the code and understand what was actually in the code. I took 3 days to work on understanding the code and then successfully executed.

### Mechanical Assembly of my Fingerprint sensor 

1. Connect the fingerprint to the USB to TTl convertor as follows:

![Connection]()

2. This is the pinout of the USB to TTL.

![pinout of the ttl converter]()

3. The pinout of the fingerprint sensor.

![pinout of the fingerprint sensor]()

4. Connections using the jumper wires: 
 
  1.Connect the GN of the sensor to the GN of the TTL converter.
 
  2.Connect the RX of the sensor to the TX of the TTL converter.
 
  3.Connect the TX of the sensor to the RX of the TTL converter.
 
  4.Connect the VCC of the sensor to the VCC of the TTL converter.

5.Then connect the sensor through the USB port of the Raspberry Pi.

### Power up

So once I assembled the hardware part, I then connected my mouse and keyboard along with the charger cable to my pi and then turned it ON. Also I need not connect the ethernet cable since I already configured the pi to connect it to the Wi-Fi. I was able to see the sensor light up. You will be able to achieve this if your hardware connection is perfect.
![power up]()

### Installation of the Raspberry Pi Fingerprint Library

We need to go to the root for some commands of the installation. I then started a terminal session and typed the following:
sudo bash

Now I added the necessary package sources:
wget -O - http://apt.pm-codeworks.de/pm-codeworks.de.gpg | apt-key add -
wget http://apt.pm-codeworks.de/pm-codeworks.list -P /etc/apt/sources.list.d/

I then had to update the available packages and install the Python library as follows:
apt-get update
apt-get install python-fingerprint --yes

Now the packages are installed and ready for testing.

### Unit Testing 

1.As mentioned above the package has files for storing a new fingerprint, reading out and deleting stored fingerprints. Now i tested the enrolling option by issueing the following:

python2 /usr/share/doc/python-fingerprint/examples/example_enroll.py

2.The terminal asks you to place the finger you want to enroll on the sensor, wait for the message "remove finger" and then again "place the same finger". 
Now the finger is given an ID and it is enrolled.

3. Now I tested whether my finger is recognized. So I issued the following script:

python2 /usr/share/doc/python-fingerprint/examples/example_search.py

4. I then put my finger on it again. If the fingerprint on the Raspberry Pi is detected, a message like this appears:

Currently stored templates: 2
Waiting for finger...
Found template at position #1
The accuracy score is: 90
SHA-2 hash of template: 3aa1b01149abf0a7ad0d7803eaba65c22ba084009700c3c7f5f4ecc38f020851

### Production testing

The testing was successful. I was able to make the sensor work by enrolling my finger, delete the finger by giving the appropriate ID, search for a fingerprint that was enrolled and retrieve the fingerprint image. This is a very reliable for security purposes. 
