---
layout: post
title:      "My Learnings - Visualization Techniques"
date:       2020-06-06 18:38:13 -0400
permalink:  my_learnings_-_visualization_techniques
---


Since my last post it has been a roller coaster of emotions from having just started with basic coding through to web scraping and data visualization. While I knew learning the ropes of becoming a data scientist was going to be challenging, I did not think it would have been this challenging. The work however, has been extremely rewarding. As complex as the work is, when you break it down line by line or look at it from a higher level, it really is not all that bad. An area that I am still working on wrapping my head around though, is the different kinds of visualization techniques and knowing when to use them. Throughout my first project with the Flatiron school, I took the time to understand how to use which ones where appropriate to help visualize the data I was trying to represent.

Just when I thought visualization techniques would be an easier section, it was not. I already knew there were multiple ways to show your data (e.g. scatter plots, bar graphs, histograms etc.). What I did not realize is that there are different visualization tools like seaborn and matplotlib (plotly). Each one offers their own benefits while, in my opinion, plotly has some downfalls.

After doing A / B testing, with plotly and seaborn for my first project, I found that seaborn aligned more strongly with the majority of my workflow, as well as visual appeal. It was not easy trying to figure this out. Again, I am brand new to coding, so mixing up the syntax for plotly versus seaborn is a commonality for me.

Seaborn visual:

<img src="https://raw.githubusercontent.com/jamesbrockb/images/master/Screen%20Shot%202021-03-04%20at%203.31.40%20PM.png">

One of the questions I created for my project was, which genre is the most profitable given the list of movies in a dataframe I created. Now the answer may seem straightforward to some, but for me, I was stuck on how I wanted to visualize it. I know I could go with your standard barplot to help show the total profits of each genre, but I was also thinking about histograms. I got lost in my train of thought and experimenting with different ways to set up this histogram, but nothing was working. This was certainly a valuable lesson for me to understand what I am trying to show and how I am trying to show it. After taking a step back and reiterating “Which genre is the most profitable?” I understood that a histogram was not going to provide me with enough insight into the solution for this question. For me, and maybe others, I tend to dive straight into the work before understanding what I am trying to solve for.

<img src="https://raw.githubusercontent.com/jamesbrockb/images/master/Screen%20Shot%202021-03-07%20at%203.24.08%20PM.png">

After taking this “new” approach, creating visuals became much more digestible. One thing I really enjoy about seaborn is how visually appealing the figures look. When I think of plotly, I think of a PC, when I think of seaborn, I think of a Mac. Now I know that is going to pull at some chords of the readers here, as I primarily see software engineers and data scientists using PC’s over Macs. As someone who has basically lived off of the OS system, I have tried toying around with a PC and it is just not for me. So that is why when I think of seaborn I think of the user friendliness and the user experience. Plus it is also very appealing to the eye, rather than plotly.

To continue the dialogue on how visually appealing seaborn is, I think it is important to talk about business presentations. While some people may prefer plotly because it provides them with the basic information they are looking for, you would want to use that plot during a business presentation. Using your own seaborn plot, with your own design is going to have a much more professional look than your standard plotly. Being a data scientist is not just about doing the work behind the desk, but also presenting your findings / strategies. You are not tasked with just putting together the data, but presenting your findings. Have a clean and professional presentation, while it may seem small, is going to have a larger impact on a potential prospect or for your executive team when reviewing this information.

All and all, whether you are using plotly, seaborn or any other form of data visualization, make sure you are answering your question and presenting your findings in an impactful way. Make sure to take a step back and look at what you are trying to solve. Take a step back and put yourself in leadership's shoes, is the presentation impactful, did I like the visuals? If you are hitting the mark on these factors, I believe you are on the right track.
