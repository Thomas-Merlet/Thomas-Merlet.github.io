---
layout: post
title: Vanadium - Online Payment Platform
date: 2018-04-15 22:13:20 +0300
description:
image: vanadium-website.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Website, ENSAM]
---

During my first and second year at the Graduate School of Mechanical and Industrial Engineering (ENSAM), I've joined the Computer Association, a team of 3 students in charge of maintaining the wifi infrastructure and making some informatics projects. 

At that time, former students have made an offline website called Vanadium to manage all the payments inside the promotions, those payments include money exchange between all students and other students union. The website was written mainly in both PHP Oriented Object and Javascript, transactions were saved on a local server accessed through SQL queries. At this time, the platform was used to save all the account balances in one place, the fiduciary money was handled by the leading students' union, creating and deleting money on the platform. We engaged with our promotion to put this useful platform online.

I will present the work done by our team, followed by a quick overview of the website for a better understanding.

# Needs

We planned different tasks to transform the platform, including:
* Migrate the platform online
* Enable secured top up by card on the platform
* Regularly notify by email members in bankrupt
* Get statistics on expenses
* Improve the global design

# Tasks

## Migrate the platform online

We subscribed to an online host server and we bought a domain name server. We migrated the website and the database to an online server, so the platform could be accessed from anywhere. As well, we optimized the size of pictures to accelerate navigation.

## Enable the secured top up

Thanks to a partnership between our school and the payment tool Lydia, we are able to pay through Lydia payment platform. We used the payment API provided by Lydia in order to integrate a payment page on our site. The main challenge was assuring the security of the transaction using transaction keys and token. We took contact with an informatics employee of Lydia to make our solution of payment secured.

## Display statistics on expense

We wanted students to access the total money spent on the site, to have an evolution of expenses view, and to know how expenses were divided between each students' union. 

## Notify members by email

We defined a list of automatic messages for different profile cases. Some of them aimed at preventing bankrupt, some other at giving information about the account status. To perform regular tasks on a server, it is common to use CRON, unfortunately our server didn't allow it.
The idea was to perform the task on page loads. During every connection, hidden to them members check whether or not they are some emails left to send. Mails are sent after the page load to keep unchanged the user experience.

## Improve the global design

We completely reshape the design of the website, from the background to the fonts in use. Our main objective was to enhance the user experience.



# Overview of the website

## Authentication page

![vanadium-authentification]({{site.baseurl}}\assets\vanadium\authentication.png)

This page secure the access at the platform to members only.


## Historic

![vanadium-historic]({{site.baseurl}}\assets\vanadium\historic.png)

Here you get a detailed overview of every past expenses, including data on dates, beneficiary organization, expense designation and amount . You can search through pages or thanks to a filter text box. The Ajax command aimed at filtering on key press directly.

## Money transfer

![vanadium-transfer]({{site.baseurl}}\assets\vanadium\transfer.png)

Here you can send some money to others or ask to receive some. We match the member searched using Ajax prediction on typing, thanks to what you can't fail paying back.

## Statistics

![vanadium-statistics]({{site.baseurl}}\assets\vanadium\statistics.png)

Some statistics on your expenses already introduced.

## Top-up your balance

![vanadium-online-payment]({{site.baseurl}}\assets\vanadium\online_payment.png)

You can fill your account using your banking card on this page. The text box is used to generate a link needed to start a transaction on Lydia's website. We authenticate every user starting a transaction with a unique code sent and returned encrypted by Lydia. Those precautions are really important to secure our website from Cross-Site Scripting [(see more about it on Wikipedia)](https://fr.wikipedia.org/wiki/Cross-site_scripting).

![vanadium-online-payment-done]({{site.baseurl}}\assets\vanadium\online_payment_done.png)
Once the payment done, we update our database with the appropriate value.

