DRAAAAAAAFT, project just started!!!!!

# Pimp-My-aquairum

In this project I show how I pimp my 30y old aquarium by replacing the old single neon tube(18W) by two new 2x LED strips (36W) plus a customised micro controller (ESP8266, Wemos mini D1) acting as quad timer and controller for multiple 240V power sockets and the LED strips.
Normally a new AQUARIUM lid with LED's or a migration LED kit costs between 80 - 170€.
I chose to order some LED strips (50cm) from CHINA shops, waiting some weeks for it.

This repository is hosting the respective Arduino Sketch for the ESP8266 mini D1.
In youtube I give a more detailed explantion to the hardware side of this project.

This repository focuses on the Arduino Code of my aquarium modernisation project.
As Control medium I am using my smartphone. As I didn't want to spend time for a web-server, I am using the RemoteYX.com app. (www.RemoteXY.com). This offers a comfortable online editor to draw the smartphone GUI, which then later is copy pasted into the code. Nevertheless, this app cost 7€ in Playstore..

Nevertheless, I tried to strucure and splitt the main code, so that an asnchrone web-server should also be implementable. Let me know, if you choose this way.

CONSTRAINTS / Problem I faced during development
1. The ESP build in NTP feature (configTime()), to periodically request time from an NTP Server has a bug. It took some time to find a work around in the net.
2. The RemoteXY has some performance issues, when too many objects are placed on a page. In my case I had to reduce the Timer display texte boxes from 16 to 4, as I got spurious display issues (some boxes were not filled spuriously). Was quite hard to troubleshoot until finding the rootcause.

How to us this Code
You have two options:
1. Simply install it, compile and reuse
You don't ahve to read my explanations to the code an should be able to simply reuse it.
If you are willing to pay for the RemoteXY app (you can use it for other projects too) and use the same hardware (ESP8266 plus same shields), you can simply download my sketch and upload it to an ESP8266 mini D1.
In the youtube video I show what components I used, how I installed them and give a deailedlist of the hardware.
Also, in this github I am providing the Arduino libraries I used (which will be soon outdated). If you don't care to have the latest library version, you can simply install them and compile my provided sketch and upload it into the ESP8266.
OR
2. Go into my code, maybe adapt it to your needs
I will try to explain below my basic structure. You can modify the code and for example implement a web-server instead for remote access, instead of teh RemotyXY app.


DETAILS to the Code
The code is split in multiple sub functions, to automise and avode redundant tasks.



