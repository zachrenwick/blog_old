---
title: "Twitter Sentiment Analysis with Azure Cognitive Services and Power BI"
date: 2020-03-05T14:45:13-07:00
description: Voice of the Customer Series - Part 2

menu:
  sidebar:
    name: Sentiment Analysis
    identifier: twitter-sentiment-analysis
    parent: azure
    weight: 10
hero: twitter-sentiment.png
tags: ["Twitter","Sentiment Analysis", "Azure"]
categories: ["Basic"]
---

**Voice of the Customer Series - Part 2**

In part 1 of my voice of the customer series blog post, I demoed how Twitter data can automatically be saved in Google Sheets using Microsoft flow.

In this post, I’ll show how you can leverage the technology from Microsoft Azure Cognitive Services to perform sentiment analysis on the tweets. This will allow you to determine how positively or negatively a brand or topic is being mentioned on Twitter. Continuing on from part 1, the demo will again include Vancouver car sharing companies.

### Why Would We Use Sentiment Analysis?
For smaller organizations, sentiment analysis may not be useful for analyzing their social media data. Perhaps you only receive a few tweets per day, and you’re very aware of your brand’s online activity.

But what if you receive hundreds, or even thousands of tweets per day? What if you have multiple social media accounts from a variety of different platforms: Instagram, LinkedIn, Glassdoor, Yelp, etc. You likely don’t have time to read each message, and it would be very difficult to try and flag posts which require extra care.

You also wouldn’t be able to consistently measure how positively or negatively your brand is trending on the internet.

Enter sentiment analysis. By assigning scores to blocks of text, this analysis allows you to measure the sentiment of each tweet/product review/social media mention.

### Introducing Azure Cognitive Services: Text Analytics
To demonstrate sentiment analysis in action, I’ve entered a negative message into the Azure text analytics API. It works by using machine learning to assign a 0% (most negative) to 100% (most positive) score based on text input it receives. As expected, my text results in a very low sentiment score of 2%.

No alt text provided for this image
Integrating Azure Cognitive Services API with Power BI
Cognitive Services will be natively integrated into Power BI premium, but not every organization can afford the $5,800+ per month price tag. With a little bit of extra work, you can still leverage the machine learning power of Azure Cognitive Services, for free. Using Power BI, we'll:

Load the Twitter data,
Send a call to the Cognitive Services Text Analytics API, and finally
Return a sentiment score for each tweet.
No alt text provided for this image
*Note: this is only proof of concept (POC) demonstration. If building this into an enterprise/production solution, you'd likely want to integrate this API into an existing social media ETL process.

Grabbing API Keys
You’ll first need to create an Azure account and setup resource groups and Azure Cognitive Services from the Azure portal. This setup is beyond the scope of this post, but you can follow along here.

Lucky for us, the free tier of Cognitive Services allows up to 5,000 transactions per month. Once you’ve set the Azure account and services up, you can grab the API keys needed through your Azure Portal: