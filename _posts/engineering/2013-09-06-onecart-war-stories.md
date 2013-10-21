---
layout: post
title: ONECart War Stories
author: Kalyan
authorTitle: Software Engineering Manager
category: engineering
picture: kalyan_j.jpg
---

We are building an exciting new product within Next Jump’s employee marketplace platform - ONECart. Our mission is to make ALL employee shopping experiences simple and helpful. While designing and engineering product features, we obsess on UX with a goal to keep it easy for consumers to check out anything while the cart is smart to apply employee pricing and all available promotions automatically.

ONECart enables smart shopping by creating a mashup of data feeds and commerce APIs from merchant partners. Behind the rapid adoption, success and growth of ONECart we also see a few stories of technical failures resulting in terrible consumer experiences.

A shopper was annoyed and felt like it was a bait-and-switch when they were charged $100 more than the display price for a tablet because the offer expired but pricing was cached 5 minutes too long. One user missed a flight and scrambled to make it to a wedding because we accidentally issued an invalid ticket from staging environments on a production system. Another instance when flowers for valentine’s day were not delivered because of a character encoding bug.

Although issues like these are few and statistically small in number - we don’t want to stop with just quantifying the occurrences and maintaining a low error rate. That’s a “corner case” is not an acceptable answer in our culture of Better Me + Better You = Better Us. The approach we apply for product engineering relies on continuous iteration and improvements to work around the challenges and limitations of API integrations every time we investigate a poor UX error. We see two big trouble areas repeatedly -  

1. Data - inaccuracy, character encoding issues 

The mindset to sanitize and validate aggressively while exchanging data even with a trusted partner saves us from a lot of trouble. Its not to say don’t trust your partner - but expect and be ready to address small differences in data compatibility and accuracy between systems. NULL values, double encoding, incomplete files - these symptoms are not intentional or planned but still happen and break entire applications if you don’t have handling.

2. Availability - uptime, load capacity, cache validity   

APIs go down – It is surprising how fragile partner systems are. Consumer shopping experience abruptly comes to a halt when an API call fails. APIs go down of a variety of reasons from communication failures to traffic loads to data errors to underlying core system failures. Build and test by corrupting the API endpoint locations and verifying a graceful degrade.

Some of these are difficult challenges but they also inspire us to innovate. Please let us know your own experiences and war stories so we learn from each other.

