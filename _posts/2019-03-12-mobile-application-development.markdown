---
layout: post
title: "Development of a Mobile application "
date: 2019-03-12 15:13:18 +0200
image: jeune_chalons_couverture.jpg
tags: [Flutter, iOS, Android]
categories: 
---

I have developped a mobile application for the town hall of Châlons-en-Champagne (France). I did this project with a teammate named BENNORA Oussama, an other student at ENSAM. 


# The Application

'Jeunes Châlons' is a free application that aims to bring together all the services provided to 15/25 year olds in the Châlons-en-Champagne area, resulting in a total of 300 pages of content, accessible by search engine or specific tabs. 


The application has multiple features among:
* A notification service to keep up to date with demonstrations and special offers for young people in the area
* A news feed organized around several categories, as well as an agenda
* The possibility of creating a dematerialized card that entitles you to specific discounts in more than 40 local businesses and services listed in the application


![iOS version of the 'Jeunes Châlons']({{site.baseurl}}/assets/jeunes-chalons/jeunes_chalons_screenshots.png)


# Technologies used

The application is entirely developped using [Flutter][Flutter], a cross plateform framework made by Google, similar to React Native.
Flutter apps are written in the [Dart][Dart] language and make use of many of the language's more advanced features.

The application uses:
* Firebase Cloud Messaging for notifications
* JSON file format for storing the data (using Firebase Database)
* Firebase Auth
* Google Maps API


[Flutter]: https://flutter.dev/
[Dart]: https://dart.dev/

# Release

The application can be seen and downloaded on the App Store and Play Store:
* [App Store][AppStore]
* [Google Play][GooglePLay]

[AppStore]: https://apps.apple.com/fr/app/jeunes-chalons/id1452875643
[GooglePLay]: https://play.google.com/store/apps/details?id=com.amje.jeuneinchalons

Since the first release, 'Jeunes Châlons' have been downloaded more than 3,000 times on both Android and iOS, and has received the "Territoire innovant" label, rewarding innovative development in France. ([see article][TerritoireInnovant])

[TerritoireInnovant]: http://www.lhebdoduvendredi.com/article/35485/l-appli-%C2%AB%C2%A0jeunes-chalons%C2%A0%C2%BB-labellisee-pour-son-cote-innovant




# Conclusion
This project was really great to gain experience in mobile application development, understanding the full conception cycle of an application and participating in the conception and design choices. 
It also helps me to gain knowledge in the Flutter framework. 


