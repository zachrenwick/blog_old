---
title: "Working with JSON Data in Power BI"
date: 2019-02-16T14:45:13-07:00
description: how you can easily analyze JSON data in Power BI. You'll also learn how to download your own Spotify listening history
menu:
  sidebar:
    name: Working with JSON Data in Power BI
    identifier: json-power-bi
    parent: power-bi
    weight: 10
hero: spotify-json.png
tags: ["PowerBI"]

---
In this article I'll give a brief overview of how you can easily work with JSON formatted data in Power BI. To keep things interesting, we'll create a simple listening history report from our JSON formatted Spotify data.


The first step in our example will source your personal data from Spotify. To do this, log onto www.spotify.com, click on "Account", and then go to your privacy settings:

Next, scroll down to your personal data. You will need to request your personal data here, and it takes a few days for Spotify to process the request. You will receive an email when the file is ready for download, and then it will appear here:


Within the zip file, you’ll notice your streaming history is the largest file from the package. This is also the data file we are interested in analyzing.


If you open up StreamingHistory, you’ll notice it’s formatted as a JSON file. In order for us to easily analyze and visualize this data, we’ll need to make some transformations in Power BI.

Transforming JSON data in Power BI to table format
Next, open up Power BI desktop and click Get Data > All > JSON > Connect:

Select the StreamingHistory file we downloaded from Spotify. You’ll then be presented with this Power Query window:

Next, click Convert To Table and select none as delimiter. Click Ok.

From here, you’ll want to split column one. Do not use original column name as prefix:

Now, you’ll notice our JSON Spotify data is finally in a usable table format. Click Close & Apply from here to load the data into Power BI:

From here, we can create basic measures and visualizations to explore all the terrible music I listen to. I’ll start with the measures:

Finally, we'll put together some basic bar and line charts to analyze song plays and listening time by artist and date:

And there we have it! You can view the interactive report hosted on the Power BI service.
