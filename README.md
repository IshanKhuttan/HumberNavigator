# BMP280(Barometric Pressure & Altitude Sensor)

<br />

##  Table of Contents

- [Introduction](#Introduction)

- [UML Diagram](#UML-Diagram)

- [Build Materials and Budget](#Build-materials-and-Budget)

- [Time Commitment](#Time-Commitment)

- [Mechanical Assembly](#Mechanical-Assembly)

- [PCB and Soldering](#Pcb-and-Soldering)

- [Unit Testing and Power Up](#Unit-testing and Power-up)

- [Finished Product](#finished-product)

- [Resources](#resources)

<br />

## Introduction
 BMP280 sensor is an environmental sensor with temperature, barometric pressure that is the next generation upgrade to the BMP085/BMP180/BMP183. This sensor is great for all sorts of weather sensing and can even be used in both I2C and SPI. This precision sensor from Bosch is the best low-cost, precision sensing solution for measuring barometric pressure with ±1 hPa absolute accuraccy, and temperature with ±1.0°C accuracy. Because pressure changes with altitude, and the pressure measurements are so good, you can also use it as an altimeter with  ±1 meter accuracy. For simple easy wiring, go with I2C. If you want to connect a bunch of sensors without worrying about I2C address collisions, then go with SPI.
 
 ![image](https://user-images.githubusercontent.com/43187006/49831322-951a8b80-fd61-11e8-95c3-a2f389499f17.png)
 
 ## UML-Diagram
 
 System Diagram
 
 ![image](https://user-images.githubusercontent.com/43187006/49844241-1ee14d80-fd90-11e8-8c42-8077f3fd24d2.png)

 
 ## Build-materials-and-Budget
 The required for my whole project is just $70, but we need parts kit which we will get in Sem1 for $120. For making the connections on the breadboard some jumper wires are required. And for the PCB you can send the gerber files to the Prototype lab and get it printed, there is no cost for the PCB. For the the case also you cand the files and get it from Prototype lab for free.  
 
 ![new budget](https://user-images.githubusercontent.com/43187006/49832284-360a4600-fd64-11e8-9098-5a0c6e5747ff.PNG)
 
 
## Time-Commitment
This schedule uses a weekly breakdown that follows the CENG 317 class schedule for the fall semester of 2018. This project could be completed in a more compact time frame if the builder so chooses. The schedule is helpful in outlining the overall flow and the order in which each milestone for the project is completed. Orignally the project was completed over a 15 week semester, But for me it took more time and I finished in week14, because I have to redesigned the PCB for atleast 4 times as I could not get the connections right. And then after my PCB was done finally then the case designing took some time as I have to design the case at [MakerCase](http://www.makercase.com) website, the download the file and upload it to the Coral Draw for making the holes and then sent it to the Protoype lab. For getting the right connections wa little bit hard, because I had the arduino(STM32F103C8T6) which is a new, so it took some time to figure out the connections.
![image](https://user-images.githubusercontent.com/43187006/49834451-69e86a00-fd6a-11e8-9a2d-3260a58b177a.png)


## Mechanical-Assembly
For making the hardware working perfectly we have to follow these instructions:

1. First we have to blink the LED of STM32 in order to check that the arduino is working properly.

2. For Uploading the Blink sketch we have to download the Arduino IDE. Then go to Tools > Boards > Boards Manager, the search the STM32 and install it. ![image](https://user-images.githubusercontent.com/43187006/49835442-30fdc480-fd6d-11e8-82b2-bf26bf93af16.png)

3. Then we need a FTDI USB to TTL Serial converter for uploading the sketch on the STM32 using a usb cable.

4. After making the connections we have to go to File > Examples > Basics > Blink, to get ino files needed for blinking and change the pin number.

![image](https://user-images.githubusercontent.com/43187006/49835951-ec732880-fd6e-11e8-8934-151a5b0cfc7e.png)
 
5. If everything is working perfectly, then we are going to make the connections of the sensor(BMP280) and Display(1.8 TFT ST7735
). 

![image](https://user-images.githubusercontent.com/43187006/49836100-74593280-fd6f-11e8-88d9-2c41508a1bec.png)

6. Then we are going to install the libraries for sensor and display, so that we can upload the sketch on Ardunio.

7. First we will go to Sketch > Include library > Manage library, then search the BMP280 and install it and open the sketch to change the pin numbers and upload it.

![image](https://user-images.githubusercontent.com/43187006/49836401-74a5fd80-fd70-11e8-951a-28e3afa0c9fe.png)

8. The check the readings if they are working properly.

![image](https://user-images.githubusercontent.com/43187006/49836424-9c956100-fd70-11e8-9f4e-5fde2299e260.png)

9. And do it similar for the display. Go to Sketch > Include library > Manage library, then search ST7735 and install it. After change the pin numbers.

![image](https://user-images.githubusercontent.com/43187006/49839301-7fff2600-fd7c-11e8-9d22-e43f2feaa61e.png)

Here are the connections on the breadboard that I have used for the Project.

![image](https://user-images.githubusercontent.com/43187006/49839420-f56af680-fd7c-11e8-9fe9-95f6f0e612ac.png)


## PCB-and-Soldering
For the PCB it was difficult part as there were lot of connections in PCB, while desinging the PCB there were lots of shorts in it. To fix the shorts I have to redesigned the PCB atleast Four times. Soldering was easy to do , but still we have to be carefull while doing the soldering we can easily burn our sensor. After designing the PCB you should send the gerber files to the prototype lab for printing the PCB and then solder the header pins to the PCB.
Here is image of the PCB and Fritzing. 
![image](https://user-images.githubusercontent.com/43187006/49840059-e3d71e00-fd7f-11e8-8633-3832877d8add.png)

![image](https://user-images.githubusercontent.com/43187006/49840089-06693700-fd80-11e8-8b57-a5effe465862.png)

Here is the image of Soldering of the Hardware:

![image](https://user-images.githubusercontent.com/43187006/49841300-12a3c300-fd85-11e8-83b3-c1ddfd856828.png)

![image](https://user-images.githubusercontent.com/43187006/49841749-ca85a000-fd86-11e8-9753-a9dfe5eb53a6.png)

## Unit-testing and Power-up
Toget the proper readings from my sensor , I have used the [bmp280test.zip](https://github.com/IshanKhuttan/HumberNavigator/files/2670358/bmp280test.zip)
) sketch that we can get after installing the library. And then after using the correct connections we can get the readings as shown below:

![image](https://user-images.githubusercontent.com/43187006/49845270-ff4c2400-fd93-11e8-9de8-a68f33ed6709.png)



## Production-Testing

For Mass Production there would be no more need to solder the sensor or the PCB manually by hand. The whole soldering process of the sensor can be covered by the use of automated machinery.The whole testing process of the sensor can be shifted from manual to automatic with  a test room designed specifically with the features of changing tempertaure,pressure,and altitude to measure the changes in the reading of the sensor.

# HumberNavigator
[HomeBoard indexArduino for STM32Projects
Blue Pill Weather Station Display](http://stm32duino.com/viewtopic.php?t=843)
