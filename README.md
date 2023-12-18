# HappyTrees
Welcome to this repository where you can find all the details about the happy tree sensor project. In the era of climate change, trees play a crucial role in urban areas by adding adaptive values. However, the public often overlooks the well-being of these vital allies. A stark example is the storm in Amsterdam in 2020, which uprooted over 500 trees due to poor living conditions, limited space, and declined biodiversity. Besides, studies also show that city trees have higher mortality rates than their forest or rural counterparts.

Happy Tree Sensor aims to retain the benefits of trees by enhancing public awareness and engagement. A group of 5 students from MADE program are developing methods to measure tree happiness using sensors and communicate it to the public, building on the Living Lab 2022 results.

With the project, we explored the answers for three questions: How can we harness the sensing technology and data science to promote the welfare and vitality of trees in urban areas? What kind of interactions can we apply to make people curious and caring about trees in the city? How can we make citizens and different sectors in the city thrive with the urban trees?

The final product contains three parts: the sensor, physical interaction, and dashboard parts. Every part serves different functions and users while interconnecting with each other. We believe that the happiness of trees is inherently intertwined with human happiness, a difference could be made if we relook at our trees from the perspective of happiness. If you want to find out more about our process please find our documentary here: https://www.youtube.com/watch?v=xZxab7wTdXg 

# Overview
In this repository you will find all the coding information needed to recreate our project, or to continue working on it in terms of code. Also find this thingiverse project page for more information about shapefiles, and installation. This repository will display how to setup the sensor. The sensors for this project can be devided into three seperate parts: 

  - Soil Unit: Seeeduino Lotus with a soil moisture sensor, temperature sensor and ESP8285 wifi module. 
  - Air unit: Adafruit ESP32 S2 feather with accelerometer, battery, LED Ring, solar panel and power management board 
  - Proximity sensor: ESP32 S2 feather witha proximity sensor

The soil unit is coded with arduino IDE and the air and proximity sensors are programmed with circuitpyhton (using MU editor). As not everything is fully functional yet (see build for more explanation) there might be multiple version of code for the same unit to optimise certain aspects of the functionality over others, depending on the use case. 

# Installation


# Run


# Build
For more details about how to recreate this project check out our thingiverse page: 
It includes all of our 3d files and further instruction on how to connect all the sensor parts, as well as the other components that are important for the happy tree project. 

At the current state of this project, the platforms (Thingspeak, Adafruit IO) that have been used pose somewhat of a problem, as the data rate that is allowed for the free plans are not enough to provide the full functionality of this project. That means that depending on what is more important ypu have to program the sensor in such a way that the data upload is working or that the interaction is working. This can likely be inproved, by only uploading the data at bigger intervals, but that removes the relevance of some sensors (eg. accelerometer)

# Contribution Guidelines
If you want to contribute please follow the below described process:

These tools are provided as-is and without warranty or support. Users are free to use, fork and modify them, subject to the license agreement.
Contact us at happytrees@ams-institute.org if you have any questions.
