---
layout: post
title:  "Three Decades of Moby Data: Raves, Remixes, and Ambient Vibes"
date:   2022-12-10
author: Nick Hamson
description: Analyzing Moby's evolving artistic style
image: /assets/images/mobyhand.jpg
---

When writing the history of electronic music in the 90's and early 2000's, it's impossible to ignore Moby's impact on the emerging genre. Over the last thirty years, his music has evolved as well. I want to chart these changes and visualize them over the course of Moby's career.

&nbsp;
# Data Collection with Spotipy and Data Cleaning
I started by using the Spotipy Python library to interface with the Spotify Web API. After setting up an an app on the Spotify Developer Dashboard, I was able to collect a list of Moby's albums, his songs, and metrics for a plethora of different audio features. This produced a list of around fifty albums and over seven hundred songs. Once I started looking through my data, however, I realized that a lot of the albums were duplicates of each other. I filtered out the duplicates and was left with thirty-three albums and just over five hundred songs, each of which had a large number of audio features: energy, danceability, loudness, key, tempo, length, and others.

&nbsp;
# Data Exploration and Visualization
As I reviewed the data I was left with, I discovered a couple trends to focus on. I realized I could group Moby's albums into three categories: mainline studio albums, remix albums with Moby's songs rearranged by other artists, and ambient music albums. I explored a few different audio features, but danceability showed the clearest trends from album to album. I used the ggplot2 package in R to create a sequential collection of boxplots, each one plotting the danceability of the songs in one of Moby's albums. According the the Spotify API, "danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable." 
It was interesting to see measurable patterns in music I've loved listening to for years, and I noticed one in particular that I marked specifically on my graphic.

![Plot](https://raw.githubusercontent.com/nickhamson/portfolio/main/assets/images/plot.png)

&nbsp;
# Heavy Beats, Heavy Living
The patterns in how danceable Moby's songs are coincide with other facets of his life and career, most notably his move to sobriety in 2008. It's easy to see the pattern before this point: Moby got his start creating heavy-hitting rave music, and his aggresive beats stayed bangin' until his drug and alcohol use hit a breaking point. After that point, the division between the different categories of album is what defines Moby's music. His studio albums are more mellow than his earlier career, and his ambient music is even more ponderous and atmospheric. Predictably, the remixed versions of Moby's albums are almost all more danceable than their studio counterparts. In general, his music has evolved to encompass a diverse array of sounds and genres.

&nbsp;

[Here is a link](https://github.com/nickhamson/web_scraping) to my code and data if you want to explore the Spotipy library or ggplot! If you want to run this code yourself, you'll need to get your own API key from the Spotify Dev site. Take a look at my previous post for more info about my process. Leave me any comments you have, and I hope you've enjoyed this dive into my favorite musician!








