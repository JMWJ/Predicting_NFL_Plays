# Predicting_NFL_Plays
The *objective* of this project is to determine if I can **predict the type of play** an offense of an NFL football team will run.

## Executive Summary
The goal for this project is to use 2 classification models - KNeighbors and Logistic Regression - to predict the type of play ran by the offense of an NFL football team. The data for this project was retrieved from [Kaggle](https://www.kaggle.com/maxhorowitz/nflplaybyplay2009to2016). Kaggle has an NFL Play-by-Play dataset from 2009 - 2016 with over 200 features that can be used for many different types of predictions and inference.
The metrics used after modeling were:
- accuracy
- recall (sensitivity)
- specificity
- precision
- confusion matrix (this helped in formulating a couple of the metrics)
All of which are explained throughout the [code](https://github.com/JMWJ/Predicting_NFL_Plays/tree/master/code) link.
Pre-modeling EDA did not give too much insight into my data. Based on a heatmap, there were no major correlations between my target variable and the features. A few histograms were added and a function known as **crosstabbing** which means to "Compute a simple cross-tabulation of two (or more) factors. By default computes a frequency table of the factors unless an array of values and an aggregation function are passed" (grabbed directly from pandas api reference). However, I had to depend on my models to do a great job at predicting. From there, I could perform post modeling EDA to gather inference. I found that the model can do a great job at predicting special teams plays in the forms of punts, kickoffs and field goals. It did a good job at predicting whether the play was going to be a running play or a passing play. Though not predicted at 100% as the special teams were, the model was still predicting run vs pass at roughly 90%.
The major limitation that is constantly run into when predicting what a coach will run is human nature. The very dynamic mind wants to throw off the defense which in turn can easily throw off a model. However, Logistic Regression did a great job on picking up on different trends in the data which allowed it to overcome most obstacles when predicting from different play set ups.

Overall, the process for this project was simple. The steps to complete this project (for the most part) were:
1. Figure out a problem
2. Determing if the data was attainable through the web or if scraping was needed
3. Munging the data
  * because of the size of the dataset, and the features that came with it, only use about 10% of the data could be used for github. also, data leakage was extremely easy to happen. As one could find [here](https://github.com/JMWJ/Predicting_NFL_Plays/blob/master/code/Cleaning.ipynb), many columns were dropped that would have had a direct impact on the predictions being guided by leaks.
4. Analysis on the data
5. Modeling
6. Post modeling EDA to gain further knowledge
7. Evaluation of the model (this was done through step 6.)

## What Future Plans Hold for This Project
In the future, I have a friend who wants to build a software that can give accurate advice for all major sports for the most popular betting platforms. ie DraftKings and FanDuel for weekly fantasy and other betting sites for over/under bets etc etc.

Thank you for taking the time to read this! If you have any advice or questions, please don't hesitate to reach out @ josephmwardjr@gmail.com
