---
layout: post
title:      "The challenge with statistics"
date:       2020-07-30 14:28:10 +0000
permalink:  the_challenge_with_statistics
---


In my most recent project, with the Flatiron School, I was tasked with Obtaining, Scrubbing Exploring, Modeling and Interpreting the data (OSEMN pronounced, 'awesome'). Sounds simple, right?  Wrong. While the first step is relatively simple, whether you are using a csv file or an API, the more difficult section comes into play with the scrubbing and exploring portion. Now while I've certainly gotten a handle on how to deal with cleaning my data set, managing the outliers making sure my model looks good, is a whole different story.

When I first went through OSEMN, I started with some very general cleaning, like removing or replacing null values and removing random strings like '?'. After this process I wanted to look over all of the data using a scatter matrix to see how all of the data may or may not correlate. After delving further into the dataset I finally came to the model using OLS. It provided me with everything I thought I needed, but once I actually plotted everything, you could see how the tails of the data were drastically far away from our 'best fit line' or 45 degree line I put in place. Which told me that my model was not that reliable. I thought I could fix this by removing some of the residuals that were sticking out like a sore thumb, but upon further discovery, I realized I needed to go all the way back to the beginning to remove the initial outliers.

This is how everything started to 'fall apart' for me, or so I thought. I think it's important to recognize that while 'going back in your code' isn't the worst thing in the world. At first it certainly seemed like it, but I believe it helps give you a better understanding of the code you're writing and the code you're trying to improve. However, herein lies the challenge I was running into. As I mentioned earlier, I needed to remove the outliers from my dataset that were impacting my tails of my model. I know there's multiple methods to remove outliers, the versions I tried were IQR (Inter Quartile Range) and the Z-Score method.

The issue I started to run into with IQR, was the utilization of IQR and boxplots. Boxplots are apparently notorious for a severe cutoff when it comes to dealing with outliers. I’m normally a very visual person which is why, naturally, I enjoy ‘seeing’ the outliers in front of me so I understand what I am solving for. So I had to scratch this method and move to the Z-Score method. Z-Score certainly made things much more simple than I thought it would. I split my data frame into two data frames. One being numerical and the other categorical. I wanted to get the Z-Score for only the numerical data and then concatenate the data frame back together.
multiple methods to remove outliers, the versions I tried were IQR (Inter Quartile Range) and the Z-Score method.
