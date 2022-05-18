# N64 -Wireless Controller Mod
A modification to your current N64 controller to make it wireless. Based on the Work by micro on the [Universal Wireless Retro Controller](https://nfggames.com/forum2/index.php?topic=5180.0)

<a href="http://www.youtube.com/shorts/WrgqsBNa95k" target="_blank"><img src="http://img.youtube.com/vi/WrgqsBNa95k/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="960" height="540" border="1" /></a>

### Notes
This project can use alot of work, mainly:
1. We could integrate the NRF24L01+ into the PCB boards.
2. Add the components of the Micolipo into the main transmitter PCB Board.
3. Translate the assembly code into arduino code to allow the use of smaller micro comtrollers and possibly 2 way communication.

## Getting Started
### Prerequisites
All the Components that are needed can be found in the bellow list:
<img src="Extra/PartsList.png"> 

One needs to have an [arduino setup as an ISP Programmer](https://docs.arduino.cc/built-in-examples/arduino-isp/ArduinoISP), or use any ISP programmer such as the [USBasp-Programmer](https://hobbycomponents.com/usb-interface/841-usbasp-avr-programmer-adaptor).

Install and set up [avrdudess](https://avrdudess.software.informer.com/2.4/) There are tons of write-ups on how to do this.

Print the Receiver's [3D box and Lid](https://github.com/saifsabban/N64-WirelessControllerMod/tree/master/3D-PrintableCase), and use two 2.5M screws to hold it down.

Print the PCBs for the [Reciever](https://github.com/saifsabban/N64-WirelessControllerMod/blob/master/N64_Receiver/N64_Receiver_PCB/N64_RX_GerberV2.1.zip) & the [Transmitter](https://github.com/saifsabban/N64-WirelessControllerMod/blob/master/N64_Transmitter/N64_Transmitter_PCB/N64_Tx_V4.0_Gerber.zip)

## Making the Reciever

Cut the N64 plug from the controller, making sure you have some length to route solder to.