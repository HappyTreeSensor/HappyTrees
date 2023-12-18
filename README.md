# HappyTrees
Welcome to this repository where you can find all the details about the happy tree sensor project. In the era of climate change, trees play a crucial role in urban areas by adding adaptive values. However, the public often overlooks the well-being of these vital allies. A stark example is the storm in Amsterdam in 2020, which uprooted over 500 trees due to poor living conditions, limited space, and declined biodiversity. Besides, studies also show that city trees have higher mortality rates than their forest or rural counterparts.

Happy Tree Sensor aims to retain the benefits of trees by enhancing public awareness and engagement. A group of 5 students from MADE program are developing methods to measure tree happiness using sensors and communicate it to the public, building on the Living Lab 2022 results.

With the project, we explored the answers for three questions: How can we harness the sensing technology and data science to promote the welfare and vitality of trees in urban areas? What kind of interactions can we apply to make people curious and caring about trees in the city? How can we make citizens and different sectors in the city thrive with the urban trees?

The final product contains three parts: the sensor, physical interaction, and dashboard parts. Every part serves different functions and users while interconnecting with each other. We believe that the happiness of trees is inherently intertwined with human happiness, a difference could be made if we relook at our trees from the perspective of happiness. If you want to find out more about our process please find our documentary here: https://www.youtube.com/watch?v=xZxab7wTdXg 

# Overview
In this repository you will find all the coding information needed to recreate our project, or to continue working on it in terms of code. Also find this thingiverse project page for more information about shapefiles, and installation. This repository will display how to setup the sensor. The sensors for this project can be devided into three seperate parts: 

  - Soil Unit: Seeeduino Lotus with a capacitive soil moisture sensor, temperature sensor and ESP8285 wifi module. 
  - Air unit: Adafruit ESP32 S2 feather with 3 axis accelerometer, battery, LED Ring, solar panel and power management board 
  - Proximity sensor: ESP32 S2 feather witha proximity sensor

The soil unit is coded with arduino IDE and the air and proximity sensors are programmed with circuitpyhton (using MU editor). As not everything is fully functional yet (see build for more explanation) there might be multiple version of code for the same unit to optimise certain aspects of the functionality over others, depending on the use case. 

# Installation
To run the code the following steps have to be taken. 
### Soil unit
The wifi module is connected through a software serial connection which is practically limited to a Baud rate of 76800, however, the wifi module is set at 115200 baud. This leads to a lot of dirty characters in the serial communication and the accompanying errors to follow. Therefore your have to establish a serial connection to the wifi module (directly connect RX and TX) and and then use AT+CIOBAUD=9600 command to change to your desired baud rate. If that doesnt work, try reflashing the wifi module first. 

Once the wifi module is set correctly, all the parts can be connected. When using thingspeak to upload the code, an account has to be made as well, and you should enter your API key in the code.  
Make sure you have installed and selected your board and libraries in the Arduino IDE. 

### Air unit
After connecting all the parts of the air unit, the ESP32 feather has to be prepared for use with circuitpython. To do this the following website can be followed: https://learn.adafruit.com/circuitpython-with-esp32-quick-start/installing-circuitpython 

### Proximity sensor
As the boards for the air unit and proximity sensor are the same the same steps can be followed as described above. 

# Run
In order to run the code, a few more steps have to be taken in the case of the air unit and proximit sensors. 

### Air unit
The thingspeak api is called on in a settings file and the wifi SSID and password are stored in a secrets file. Dont forget to create both of these files as well. Secondly remember to install all the relevant libraries by downloading the adafruit circuitpython library packages and copying the libraries that are relevant to the lib folder on the CIRCUITPY drive. 

### Proximity sensor

For the proximity sensor the 

# Build
For more details about how to recreate this project check out our thingiverse page: 
It includes all of our 3d files and further instruction on how to connect all the sensor parts, as well as the other components that are important for the happy tree project. 

At the current state of this project, the platforms (Thingspeak, Adafruit IO) that have been used pose somewhat of a problem, as the data rate that is allowed for the free plans are not enough to provide the full functionality of this project. That means that depending on what is more important ypu have to program the sensor in such a way that the data upload is working or that the interaction is working. This can likely be inproved, by only uploading the data at bigger intervals, but that removes the relevance of some sensors (eg. accelerometer)

# Contribution Guidelines
If you want to contribute please follow the below described process:

These tools are provided as-is and without warranty or support. Users are free to use, fork and modify them, subject to the license agreement.
Contact us at happytrees@ams-institute.org if you have any questions.
