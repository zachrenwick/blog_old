---
title: "Automatically Save Twitter Data to Google Sheets with Microsoft Power Automate"
date: 2019-03-16T14:45:13-07:00
description: 

menu:
  sidebar:
    name: Twitter to Google Sheets Integration with Power Automate
    identifier: power-automate-google-sheets
    parent: azure
    weight: 10
hero: googlesheets-pa.png
tags: ["Twitter","Sentiment Analysis", "Azure"]
---

**Voice of the Customer Series - Part 1**

In this tutorial I’ll demonstrate how to set up a Microsoft Power Automate to automatically save tweets that mention your brand, product or service to a Google Sheet.

In a future post I’ll show how you can then explore this Twitter data and perform sentiment analysis on the tweets. This will allow you to evaluate how positively or negatively users are tweeting about your brand.

To start, navigate to the Microsoft Power Automate homepage and select the “Save Tweets to a Google Sheet” template.


Once you select this template, you’ll need to connect your Twitter and Google accounts. After you’ve authenticated these accounts, click continue.


Outside of Microsoft Power Automate, you’ll also need to set up a Google Sheet with headings for the Twitter data fields you’ll be collecting. I decided to collect the below fields:


Next, you’ll enter the search terms used to save tweets. I’m going to be analyzing tweets mentioning the Vancouver car share provider @EvoCarShare,but you can select whichever search terms you’d like to track.


Select the Google Sheet file in the “Insert Row” user interface, and then map each of your required Twitter data fields to the Google Sheet columns below. Microsoft Power Automate makes this incredibly easy, as the interface shows all of the fields available to you. Once you’ve mapped all of your required fields, press save.


Once you’ve enabled your Flow, you can check in the run history and perform a test to ensure the process is working properly. As you can see from the run history and the Google Sheet I set up, the automation is working correctly, and tweets are successfully saved whenever they mention @EvoCarShare.


In my next post I’ll show how you can add on from this integration, to analyze how positively or negatively users are mentioning your brand on Twitter.

Until then, you can explore the Twitter data in my Google Sheet below!