Automated Plant  Watering System
As a project work for Course

INTRODUCTION TO INTERNET OF THINGS(IOT) (ECE217) 
Submitted By :
Abhishek Kumar
12010299
Submitted To :
DR.SOMEET SINGH
 (17380 ) 
Lovely Professional University



TABLE OF CONTENT
1.	INTRODUCTION	3
2.	ACKNOWLWDGEMENT	4
3.	HARDWARE REQUIREMENTS	5-12
4.	SCREENSHOTS	12
5.	 FLOW DIAGRAM 	13
6.	METHODOLOGY	      14
7.	CONCULSION	       15



INTRODUCTION

 In our daily fast paced life, we ignore many things that we need to take care of. But ignoring of something living might result in the death of that. So are the plants, if we, because of any reason, forgot to take care of the plant or even forgot to water the plant, might result as the end of life of that plant. Plants need special care and thanks to today’s advancement in technology, giving of that special care is possible. We can give that through automated plant watering system. Having Arduino Uno as the main controlling unit of the system, this system performs the following tasks:

1.	Supply water according to the moisture level
 2. Display the Temperature and Humidity on LCD
3.It also send the soil moisture, temperature and humidity level on cloud for future analysis.


ACKNOWLEDGEMENT


We have taken a lot of effort into this project. However, completing this project would not have been possible without the support and guidance of a lot of individuals. We would like to extend our sincere thanks to all of them. I Would like to express my deepest gratitude to my Teacher DR..SOMEET SINGH
for contributing their valuable time and efforts in helping me out with this project. We would like to thank him for providing the necessary information and resources for this project. We would like to express our gratitude towards our parents & our friends for their kind co-operation and encouragement which help us a lot in completing this project. Our thanks and appreciations also go to our colleague in developing the project. Thank you to all the people who have willingly helped us out with their abilities



II. HARDWARE REQUIREMENTS


1.Arduino Uno
Arduino is an open-source electronics platform based on easy-to-use hardware and software. The Arduino software is easy-to-use for beginners, yet flexible enough for advanced users. It runs on Mac, Windows, and Linux. Teachers and students use it to build low cost scientific instruments, to prove chemistry and physics principles, or to get started with programming and robotics.
•	The operating voltage is 5V
•	The recommended input voltage will range from 7v to 12V
•	Digital input/output pins are 14
•	Analog i/p pins are 6
•	DC Current for each input/output pin is 40 mA
•	DC voltage- 3.3V 
•	Flash Memory is 32 KB
•	SRAM is 2 KB
•	EEPROM is 1 KB
•	CLK Speed is 16 MHz
 
2.DHT11(Temp. & Humidity)
The DHT11 is a basic, ultra low-cost digital temperature and humidity sensor. It uses a capacitive humidity sensor and a thermistor to measure the surrounding air and spits out a digital signal on the data pin (no analog input pins needed). It's fairly simple to use but requires careful timing to grab data. The only real downside of this sensor is you can only get new data from it once every 2 seconds, so when using our library, sensor readings can be up to 2 seconds old.IT has 3 pins , VCC,GND,DIGITAL PIN.  


 
  3.Soil Moisture Sensor: 
The soil moisture senses the moisture content in the soil and        based on the value that is showed on the display, according to the control circuit motor will be start ant it will pump the water with the help of a pump and the pumping actions will continue till it fulfills the conditions and with the help of the sensor we will get to know about when soil is more dryer than the other time zone and same for wet conditions.
 

4.ESP8266(WIFI MODULE)
Wi-Fi is uniquely placed to support broadband and narrowband IoT applications from a common platform that can work at varying levels of power consumption and signal range.
	The ESP8266 is a low-cost Wi-Fi microchip, with built-in TCP/IP networking software, and microcontroller capability
The ESP8285 is a similar chip with a built-in 1 MiB flash memory, allowing the design of single-chip devices capable of connecting via Wi-Fi.[4]
These microcontroller chips have been succeeded by the ESP32 family of devices.

•	Integrated with a 32-bit Tensilica® processor
•	Based on the IEEE 802.11
•	CH_PD=3.3V
•	VCC=3.3V
Pin details:
•	GND is the Ground Pin and needs to be connected to GND pin on the Arduino.
•	IRQ is an interrupt pin that can alert the microcontroller when RFID tag comes into its vicinity.
•	MISO / SCL / Tx pin acts as Master-In-Slave-Out when SPI interface is enabled, acts as serial clock when I2C interface is enabled and acts as serial data output when UART interface is enabled.
•	MOSI (Master Out Slave In) is SPI input to the RC522 module.
•	SCK (Serial Clock) accepts clock pulses provided by the SPI bus Master i.e. Arduino.
•	SS / SDA / Rx pin acts as Signal input when SPI interface is enabled, acts as serial data when I2C interface is enabled and acts as serial data input when UART interface is enabled. This pin is usually marked by encasing the pin in a square so it can be used as a reference for identifying the other pins.



5.POWER SUPPLY:
For power supply we are using 9v dc battery basically we have to two different voltage required components one is working on 5v and second is working on 3.3v.
The WIFI module esp8266 need a working voltage of 3.3v and Arduino ,16X2 I2C LCD, SOIL MOSITURE SENSOR, DHT11 is working on 5v power supply and we are taking supply from Arduino pins


6.I2C 16x2 LCD DISPLAY:
I2C_LCD is an easy-to-use display module, It can make display easier. Using it can reduce the difficulty of make, so that makers can focus on the core of the work. We developed the Arduino library for I2C_LCD, user just need a few lines of the code can achieve complex graphics and text display features.
for displaying the temperature,humidity,soil moisture and when pump is on/off we are using lcd with I2C comunication(I2C protocols).
I2C is two wire comunication (SDA,SCLK) 
7.water pump:
we are using 9-12v dc water pump to supply the water to the plants and we are giving 9v power supply to the motor connecting it with a relay switch so when soil moisture sense that soil is dry it will active the actuators (water pump) and water pump will supply wat 
Pin-config

Ardiuno pins	hardware
A0	Soil mositure
Pin 7	Dc motor
Pin 8	DHT11
A4,A5	LCD
Pin 3,2	Esp8266
