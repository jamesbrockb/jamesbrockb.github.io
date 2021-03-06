---
layout: post
title:      "The challenge with statistics"
date:       2020-07-30 10:28:11 -0400
permalink:  the_challenge_with_statistics
---


In my most recent project, with the Flatiron School, I was tasked with Obtaining, Scrubbing Exploring, Modeling and Interpreting a data set(OSEMN pronounced, 'awesome'). Sounds simple, right? Wrong. The data set we were working with was specifically for the housing prices of Kings County in Washington State. The data set covered a multitude of features about a home or in a home. Such as bathrooms, the view it has, or even the square footage of the 15 homes nearest to you. While the first step of OSEMN is relatively simple, whether you are using a csv file or an API, the more difficult section comes into play with the scrubbing and exploring portion. Now while I've certainly gotten a handle on how to deal with cleaning my data set, managing the outliers making sure my model looks good, is a whole different story.

When I first went through OSEMN, I started with some very general cleaning, like removing or replacing null values and removing random strings like '?'. After this process I wanted to look over all of the data using a scatter matrix to see how all of the data may or may not correlate. After delving further into the dataset I finally came to the model using OLS. It provided me with everything I thought I needed, but once I actually plotted everything, you could see how the tails of the data were drastically far away from our 'best fit line' or 45 degree line I put in place. Which told me that my model was not that reliable. I thought I could fix this by removing some of the residuals that were sticking out like a sore thumb, but upon further discovery, I realized I needed to go all the way back to the beginning to remove the initial outliers.

This is how everything started to 'fall apart' for me, or so I thought. I think it's important to recognize that 'going back in your code' isn't the worst thing in the world. At first it certainly seemed like it, but I believe it helps give you a better understanding of the code you're writing and the code you're trying to improve. However, herein lies the challenge I was running into. As I mentioned earlier, I needed to remove the outliers from my dataset that were impacting my tails of my model. I know there's multiple methods to remove outliers, the versions I tried were IQR (Inter Quartile Range) and the Z-Score method.

The issue I started to run into with IQR, was the utilization of IQR and boxplots. Boxplots are apparently notorious for a severe cutoff when it comes to dealing with outliers. I’m normally a very visual person which is why, naturally, I enjoy ‘seeing’ the outliers in front of me so I understand what I am solving for. So I had to scratch this method and move to the Z-Score method. Z-Score certainly made things much more simple than I thought it would. I split my data frame into two data frames. One being numerical and the other categorical. I wanted to get the Z-Score for only the numerical data and then concatenate the data frame back together.

Data before being normalized:
<img src="https://raw.githubusercontent.com/jamesbrockb/images/master/not%20normalized.png">

Z-Score normilization:
<img src="https://raw.githubusercontent.com/jamesbrockb/images/master/zscore.png">

Data after being normalized:
<img src="https://raw.githubusercontent.com/jamesbrockb/images/master/normalized.png">

Once this was completed I went back through all my steps of looking over the data again. Things look a lot more normalized (from my normalization processes I didn’t mention) once I removed the outliers in my numerical data. I again ran into an issue where my R Squared dropped from .7 to .56. While this still ‘passes’ I wasn’t satisfied. I know my R Squared suffered because I removed some of the data, but I wasn’t expecting it to drop so significantly. I was now tasked with strategizing on how to go back to where I was, while using the data I had. I didn’t want to add the outliers back, do I normalize it further using things like log transformation? I run risks though with the different options I have. Some may make the data look better, but the accuracy could suffer.

Now I know the industry standard is >.5 but we were tasked to try and achieve .8. Little did I know though, that I had one particular column that was manipulating my data unfavorably. It was the zip codes column in particular. The reason this was happening was because I was treating it as if it was a numerical piece of data rather than categorical. Why choose this initially? I don't know, I'll blame it on me still being so green in this field. Once I (my instructor helping me) came to this realization and moved my zip codes into my categorical set of information, everything changed. My R^2 increased to .83! I was astonished that something that seemed so simple could have that big of an impact on my data. I was looking in all the wrong places trying to solve for my R^2 dilemma, but there was no end in sight.

After this was complete, I was finally able to look at all of my coefficients, knowing they were accurate, to help answer some of the questions I had with this project. Like what about a house makes it so expensive in this county? Turns out that the ones with the largest impact were the number of bathrooms, the grade of the home and the zipcode you lived in. Now that I was confident with the work I put in (and the proof was in the pudding my my R Squared being .83) I could make recommendations to my ‘client’. Overall the project wasn’t horrible, I feel like more and more data science is becoming more of a mental challenge than execution challenge. I find myself overthinking when in most cases it’s the simplest solution. I’m hoping in my next project which covers machine learning, that I won’t be overthinking as much. 
