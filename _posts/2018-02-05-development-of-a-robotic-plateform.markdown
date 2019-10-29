---
layout: post
title: Development of a robotic platform
date: 2018-02-05 22:13:20 +0300
description:
image: robotic-plateform.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Robotics, ENSAM]
---

During my second year at the Graduate School of Mechanical and Industrial Engineering (ENSAM), I've worked on a group project consisting of creating a mobile robotic platform, allowing future promotion to compete in the [French Robotics Cup](https://www.coupederobotique.fr/).
The robot is moving inside a closed area, and must achieve certain actions such as picking object. It must be able to locate itself on the area. 

If you want to understand all choices we made in order to fulfill this conception, you can read the following report or look at the support of the oral presentation associated.

* [Download the Report][Robotic Platform Report]
* [Download the Support of the Presentation][Robotic Platform Presentation]

[Robotic Platform Report]:{{site.baseurl}}/assets/robotic-plateform/Report.pdf
[Robotic Platform Presentation]:{{site.baseurl}}/assets/robotic-plateform/Slides.pdf


# Objectives

This project was based on an Arduino Robot card, and we used the Arduino Development environment to program the robot. The goal of this project was to implement the base features needed to compete at the cup including:
* Implementation of a Bluetooth connection
* Development of a positioning system using laser
* Obstacle avoidance algorithm


# Integration of Bluetooth Low Energy (BLE)

My main work for this project was the integration of Bluetooth Low Energy, using a BLE card sold by Adafruit, the [Adafruit Bluefruit LE Shield](https://www.adafruit.com/product/2746).

![Card]({{site.baseurl}}/assets/robotic-plateform/bluetooth.jpg)

![Wiring]({{site.baseurl}}/assets/robotic-plateform/electrical.png)

I've created a Android application allowing the Bluetooth connection using BLE, and sending command over the bluetooth channel. The app was in the first part a demo for manual control of the robot, and was helpful to recieve data from the positioning system of the robot.

![Android App]({{site.baseurl}}/assets/robotic-plateform/app.png)

# Positioning system

The positioning system was developed by the other member of the team and was using a 3 points method and was using laser and the bluetooth connection to reveive data from the 3 sensors. 

![Positioning System]({{site.baseurl}}/assets/robotic-plateform/position.png)

# Conclusion

This project was really great to gain experience in the robotic field. It also helped me to gain experience in Arduino and robotic development, and prototyping. 






