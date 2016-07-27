#Seeeduino Stalker V3.1
##Introduction
----

Maybe you are very familiar with the seeeduino stalker series, or maybe you are totally new to this feature rich Wireless Sensor Network Node. No matter what situation you are in, if you are going to make an outdoor data-logging application, you will find that Seeeduino Stalker is the best board.

The main purpose of creating this series is to create an X-bee carrier board so that users can make outdoor application more conveniently. Ever since the first version be released in 2009, Seeeders has been continuously collecting feedback from users and kept upgrading the board. there are 6 versions ever existed during the past 7 years, this summer we are excited to release the most updated member of the Seeeduino stalker family----Seeeduino Stalker V3.1.

Seeeduino Stalker V3.1 is not just a simple update of V3.0.The main surprise you'll find about the board is impressively low power consumption, in sleep mode, the output current of the whole board will be as low as 100uA,This is an upgrade truly derived from users feedback.(we really care about your opinion).let's see how we achieve it.

![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Stalker_V3_1/master/images/cover.JPG)

**Optimize RTC Circuitry**

Comparing to V3.0, RTC module of V3.1 can only be powered by button cell instead of powered by both button cell and lithium battery. So that power of the lithium battery can be saved from supplying RTC.

**Improve Power Management**

In V3.1, when MCU is in sleep mode, all other power supplement, including Bee area port, 3.3v port, VCC can be cut off manually, so that power can really be saved.

**Other Changes**

There is a toggle switch added to X-bee area, which allows you to select either the hardware serial port   or software serial port base on what you want to connect.

We also added 2 toggle switch on RTC circuitry corresponding 2 INT pin of MCU, so that users can easily choose which INT pin to be connected with RTC INT port then activate MCU.

[![Get one now](https://github.com/SeeedDocument/Wio_Node/raw/master/pictures/300px-Get_One_Now_Banner.png)](http://www.seeedstudio.com/Seeeduino-Stalker-V3.1-p-2686.html)

##Features
----
- Compatible with Seeeduino (I/O ports use 3.3V Logic). Can be programmed with Arduino Processing language.
- Onboard Real Time Clock chip **DS1337S** (Socket for a CR1220 coin cell, which acts as a backup power source for RTC)
- Serial interface with DTR for auto reset during programming when operating in standalone mode. (For programming, UartSBee is not included).
- microSD card socket
- I2C Pin header (operation voltage is selectable: 5.0V or 3.3V)
- Grove connector (operation voltage is selectable: 5.0V or 3.3V)
- Reset buttons for XBee Modules and ATMega328P
- **Bee series socket** 2*10 pin 2.0mm pitch (which will mate with one at a time any of the wireless modules: XBee, BluetoothBee, GPSBee or RFBee.)

##Specicication
----

|Parameter|Value|
|-------------------	----|---------------|
|Micro Controller 		|Atmega328P    	|
|Clock Speed      		|8 MHz         	|
|I/O Voltage      		|3.3V          	|
|RTC			  		|DS1337S		|
|Board for Arduino IDE	| Arduino Pro or Pro Mini (3.3v , 8 MHz)w/ATmega328	|
|Power Supply			|3.7v LiPo Battery, Use 5VDC solar panel for charging the battery|
|Power Connector		|2 pin JST/ USB|
|Connectivity			|I2C, UART, SPI|
|SD Card   				|micro SD card |
|Open Circuit Current	|6 mA max|
|Charging Current		|300mA|
|Maximum Current on 3.3v port |	800mA|
|Size of PCB 			|86.74mm x 60.96mm|

##Application Ideas
----

- Wireless Sensor Network (using [XBee](http://www.seeedstudio.com/wiki/XBee_Pro_Series2_RF_module) bought separately)
- GPS Logging (using [GPSBee](http://www.seeedstudio.com/wiki/GPS_Bee_kit) bought separately)
- Data Acquisition System capable of communicating with an App running on iPhone/Android Phone (using [BluetoothBee](http://www.seeedstudio.com/wiki/Bluetooth_Bee) bought separately).
- RF Remote Control (using [RFBee](http://www.seeedstudio.com/wiki/RFbee_V1.1_-_Wireless_Arduino_compatible_node) bought separately).
- As a simple standalone Arduino compatible physical computing platform.



##Get Started
----
If this is your first time to program with a Seeeduino Stalker. You can follow the below steps to getting started. Before we start, make sure you have the below things on hand:

|Seeeduino Stalker V3.1|UartSBee V4|Mini USB Cable|6pin Cable|
|----------------------|-----------|--------------|----------|
|![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Stalker_V3_1/master/images/gs_stalker.JPG)|![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Stalker_V3_1/master/images/gs_uartsbee.jpg)|![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Stalker_V3_1/master/images/gs_miniusb.jpg)|![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Stalker_V3_1/master/images/gs_6pincable.jpg)|
|[GET ONE NOW](http://www.seeedstudio.com/Seeeduino-Stalker-V3.1-p-2686.html)|[GET ONE NOW](http://www.seeedstudio.com/UartSBee-V4-p-688.html)|[GET ONE NOW](http://www.seeedstudio.com/Mini-USB-cable-100cm-p-252.html)|[GET ONE NOW](http://www.seeedstudio.com/6-pin-dual-female-jumper-wire-300mm-(5-PCs-pack)-p-128.html)|

!!!Note
    UartSBee V4, Mini USB Cable and 6pin cable are not included. 

###STEP1: Hardware Connection

|Seeeduino Stalker|UartSBee V4|
|-----------------|-----------|
|	DTR			  |	DTR		  |
|	TXD			  |	RXD		  |
|	RXD			  |	TXD		  |
|	5V			  |	VCC		  |
|	GND			  |	GND		  |

!!!Note
	The power switch on UartSbee V4 put to 5V	

###STEP2: UartSBee and the Driver

UartSBee is a USB to Serial UART interface which is based on FT232RL from FDTI. Click to download the [driver](http://www.ftdichip.com/FTDrivers.htm) for the board.

In our case, it will perform three functions:

- To program the Seeeduino Stalker.
- To communicate with Seeeduino Stalker.
- Provide power (from USB power of PC) to Seeeduino Stalker (including any peripherals connected to it).

###STEP3: Arduino IDE

Seeeduino Stalker is an Arduino compatible board that with rich function. If you don't have an Arduino IDE, you need to download the latest Arduino software to program the board. 

![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Stalker_V3_1/master/images/Download_IDE.png)

###STEP4: Blink

Here we will update a simple code to Stalker. Open your Arduino IDE, open **File > Examples > Basics > Blink**

![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Stalker_V3_1/master/images/arduino_blink.png)

Then click on the Upload button, seconds later after the uploading is done, check **L** on the board, it will blink at the frequency of 1s.
