#Seeeduino Stalker V3.1
##Introduction
----

Maybe you are very familiar with the seeeduino stalker series, or maybe you are totally new to this feature rich Wireless Sensor Network Node. No matter what situation you are in, if you are going to make an outdoor data-logging application, you will find that Seeeduino Stalker is the best board.

The main purpose of creating this series is to create an X-bee carrier board so that users can make outdoor application more conveniently. Ever since the first version be released in 2009, Seeeders has been continuously collecting feedback from users and kept upgrading the board. there are 6 versions ever existed during the past 7 years, this summer we are excited to release the most updated member of the Seeeduino stalker family----Seeeduino Stalker V3.1.

Seeeduino Stalker V3.1 is not just a simple update of V3.0.The main surprise you'll find about the board is impressively low power consumption, in sleep mode, the output current of the whole board will be as low as 100uA,This is an upgrade truly derived from users feedback.(we really care about your opinion).let's see how we achieve it.

**Optimize RTC Circuitry**

Comparing to V3.0, RTC module of V3.1 can only be powered by button cell instead of powered by both button cell and lithium battery. So that power of the lithium battery can be saved from supplying RTC.

**Improve Power Management**

In V3.1, when MCU is in sleep mode, all other power supplement, including Bee area port, 3.3v port, VCC can be cut off manually, so that power can really be saved.

**Other Changes**

There is a toggle switch added to X-bee area, which allows you to select either the hardware serial port   or software serial port base on what you want to connect.

We also added 2 toggle switch on RTC circuitry corresponding 2 INT pin of MCU, so that users can easily choose which INT pin to be connected with RTC INT port then activate MCU.

Just like every other revises, we fixed a few bugs.




[![Get one now](https://github.com/SeeedDocument/Wio_Node/raw/master/pictures/300px-Get_One_Now_Banner.png)](http://www.seeedstudio.com/Seeeduino-Stalker-V3.1-p-2686.html)



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