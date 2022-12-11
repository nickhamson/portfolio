---
layout: post
title:  "Extreme APIs: Spotify in Python"
date:   2022-10-25
author: Nick Hamson
description: Using the Spotipy library and the Spotify Web API to gather audio data about Moby's discography
image: /assets/images/moby-wide.jpg
---

Intro paragraph

&nbsp;
# The Spotify Web API and Spotipy
[Spotipy](https://spotipy.readthedocs.io/en/master/#) is a simple Python library for interacting with the Spotify Web API. It was easy to install and use once I got my authentication keys set up. I won't write a whole tutorial, but [here are the basic steps](https://github.com/nickhamson/web_scraping) I took to get my data:
1. Register an app on the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications)
2. Use the Client ID and Client Secret Key they gave me to instantiate an authenticated Spotify object
3. Use Moby's Spotify URI to request his album information
4. Pull track IDs from each album, and then pass those IDs into the audio_features function
5. Compile that list into a useful pandas DataFrame and csv file

&nbsp;
# Ethics
Spotipy is an established library that was suggested on Spotify's list of packages that utilize their API. I read through the [Spotify Developer Terms of Service](https://developer.spotify.com/terms/) and the simple data-fetching I'm doing here is compliant with their terms.

&nbsp;
# Take a look for yourself!

[Here is a link](https://github.com/nickhamson/web_scraping) to my repository and the code I used. If you want to run this code yourself, you'll need to get your own API key from the Spotify Dev site. My dataset has a lot of interesting info I'm excited to look at! Spotify has analytic data on metrics like danceability, instrumentalness, acousticness, and energy. I'm planning on seeing how these attributes have changed over time in Moby's music, and hopefully I can see some cool trends in some of my favorite music!

&nbsp;
Let me know in the comments what patterns you think I should look for in my analysis!






