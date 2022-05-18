# N64 -Wireless Controller Mod
A modification to your current N64 controller to make it wireless. Based on the Work by micro on the [Universal Wireless Retro Controller](https://nfggames.com/forum2/index.php?topic=5180.0)

<p align="center">
<a href="http://www.youtube.com/shorts/WrgqsBNa95k" target="_blank"><img src="/Extra/Images/Face.png" 
alt="IMAGE ALT TEXT HERE" width="960" border="1" /></a>
<p>

### Notes
This project could use a lot of work, mainly:
1. We could integrate the NRF24L01+ into the PCB boards.
2. Add the components of the Mico-LiPo into the main transmitter PCB Board.
3. Translate the assembly code into Arduino code to allow the use of smaller micro controllers and possibly 2 way communication.

Know that if you decide to undertake this project, you are the one liable for any damages or risks that might occur.

## Getting Started
### Prerequisites
All the Components that are needed can be found in the bellow list:
<p align="center"><img src="Extra/PartsList.png"><p>

Optionally you could use JST connectors, instead of soldering wires directly to the PCB. I used the PH series.<br/>
you need to have an [ISP Arduino Programmer](https://docs.arduino.cc/built-in-examples/arduino-isp/ArduinoISP), or use any ISP programmer such as the [USBasp-Programmer](https://hobbycomponents.com/usb-interface/841-usbasp-avr-programmer-adaptor).<br/>
Install and set up [avrdudess](https://avrdudess.software.informer.com/2.4/) There are tons of write-ups on how to do this.<br/>
Print the Receiver's [3D box and Lid](https://github.com/saifsabban/N64-WirelessControllerMod/tree/master/3D-PrintableCase), and use two 2.5M screws to hold it down.<br/>
Print the PCBs for the [Reciever with a SMD microcontroller](https://github.com/saifsabban/N64-WirelessControllerMod/blob/master/N64_Receiver/N64_Receiver_PCB/N64_RX_GerberV2.1.zip) or [Reciever with a DIP microcontroller](https://github.com/saifsabban/N64-WirelessControllerMod/blob/master/N64_Receiver/N64_Receiver_PCB/N64_RX_GerberV2.0.zip) & the [Transmitter](https://github.com/saifsabban/N64-WirelessControllerMod/blob/master/N64_Transmitter/N64_Transmitter_PCB/N64_Tx_V4.0_Gerber.zip)

## Making the Receiver
1. Populate the Receiver PCB with the appropriate parts (The essential resistors & capacitor can be either SMD or Through-Hole):<br/><p align="center"><img src="N64_Receiver/RXParts.png"><p>
2. Connect the ISP pins for your desired programmer to the Receiver Board. Hopefully this image and the silkscreen will be of some help.<br/><p align="center"><img src="N64_Receiver/N64_RX.png" alt="drawing" width="800"/><p>
3. Program the Board using AVRdudess with the same parameters shown, MAKE SURE THAT THE HIGH BYTE IS 0xDF & LOW BYTE IS 0xEE. If you don't then you might never be able to use that microcontroller again unless you change the crystal<br/><p align="center"><img src="N64_Receiver/ArduinoAsSP.png" alt="drawing" width="500"/><p>
4. Solder some wire to the switch, and solder the other side to the PCB board's SW connector (It doesn't matter which pole of the switch connects to which pad).
5. Cut the N64 plug from the controller, making sure you have some length to route & solder to, I usually keep amount 20cm of cable and cut as necessary.
6. Check the fit of the plug to the printed box, some 3D printers make the opening too large or too small.
7. Glue the Connector to the BOX.
8. Solder the Red wire to the + pad on the connector labelled N64, the black wire to the pad labelled - and the white wire to the pad in the middle of both + & -.
9. Attach (or solder) the NRF24L01+ board onto the Receiver PCB.
10. Place and glue all the parts inside the 3D printed box (As shown) and screw on the Lid<br/><p align="center"><img src="/Extra/Images/1.jpg" alt="drawing" width="250"/><p>

## Making the Transmitters
1. Populate the Transmitter PCB with the appropriate parts:<br/><p align="center"><img src="N64_Transmitter/TXParts.png"><p>
2. Connect the ISP pins for your desired programmer to the Transmitter Board. Hopefully this image will be of some help (the pins are in the same location as the connector on the Transmitter PCB, the Ground pin is the one highlighted)<br/><p align="center"><img src="N64_Transmitter/N64_TX.png" alt="drawing" width="800"/><p>
3. Program the Board using AVRdudess with the same parameters shown, MAKE SURE THAT THE HIGH BYTE IS 0xDF & LOW BYTE IS 0xDF. If you don't then you might never be able to use that microcontroller again unless you change the crystal<br/><p align="center"><img src="N64_Transmitter/ArduinoAsSP.png" alt="drawing" width="500"/><p>
4. Disasemble the N64 Controller.
5. Desolder the original blue connector that connects to the cable. (I would strongly advise soldiring a JST 4 pin PH female connector) as shown in the photo below<br/><p align="center"><img src="/Extra/Images/22.jpg" alt="drawing" width="250"/><p>