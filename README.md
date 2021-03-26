<p align="center">
 <img width="900" height="500" src=images/nba_logo.jpg>
 </p>

# NBA Game Prediction
Predicting the outcome of any given NBA game


## Overview
As the sport of basketball has becoming increasingly popular, data has come to the forefront for analyzing player and team performance. NBA owners will do anything to garner an advantage over their opponents,  and players look to managers and coaches to help them improve through insight on relevant data. 

Bettors also look to statistics to better inform themselves of what the potential outcome of a game may be. Using NBA statistics from basektball-reference.com over the past 18 years, we created a model to predict whether the home team would win a given match based on their previous statistics. We use strictly Team data in each model.

## Business Problem
Mark Cuban, owner of the Dallas Mavericks, has been contemplating hiring and outside analytics consultant as his team has been on quite a long losing streak. Cuban doesn't know what is going wrong and is hoping someone with a strong analytics background can help him understand their teams issues. Several outside consultants are pitching to him and we are one of them! We decided to create a model to help predict why any given NBA team may win a game to help him understand why his team may be losing.

## Data

To understand the NBA as a whole, we decided to do some league research and exploratory analysis to better understand the data we are analyzing. Developing our domain knowledge was important in order to be able to succinctly analyze our data. Using basketball-reference.com as our datasource, we obtained game data for each team over the past 18 years (over 23,000 observations). Before featurn engineering, our data had over 70 columns (features) of information relating to a specific game played.

<p align="center">
 <img width="700" height="500" src=images/home_team_advantage.png>
 </p>
 
## Methods

### Cleaning and Feature Engineering

This project uses data cleaning and feature engineering. Cleaning our data was important in order to analyze it. Many of the win-loss records of each team were in the wrong data type (strings) and needed to be converted in order to use them within our model. Almost all features in our model were engineered and not taken directly from our sourced data. We engineered features that showed the last ten games a team had played and average those stats out in order to predict how they would play in an upcoming game. We also created a feature that show the disparity between two teams, which significantly helped our model. Cleaning our data and building these features helped make our model more interpretable and significant.

As all of our data was in game format, we feature engineered our data so that it would show how well a team has played over the past 10 games (rolling averages of points, assists, rebounds, field goal percentage, etc.) for both the home team and away team. This made the model more predicitive and would be more interpretable for any NBA team or any bettor looking going into a game.

One important note is that we decided to resample our model as one outcome was roughly 60% of our data and the pther was 40%. By resampling, we evenly distributed each outcome, bringing our baseline to 50%

## Results

Our simplest model, Logistic Regression, came back with a confusion matrix that produced a 64% accuracy score. For our purposes, we were looking to maximize accuracy as we were solely focused on how accurately we could predict the outcome of a given game. We were not focuse on false negative or false positives. 

Our KNN classifier was our worst model, posting an accuracy score of around 54% (very close to our baseline). We ran through six different models altogether (Logistic Regression, KNN Classifier, Decision Tree, Random Forest, Adaboost, Gradient Boost) and used grid searches for each one to find their optimal parameters. Through running each model, Adaboost gave us the best result, with an accuracy score of 66.5%. This was 16.5% over our baseline, meaning that this model significantly out performed no model at all. Below are the confusion matrix for both our simple model (Logistic Regression) and our final model (Random Forest).

 
#### Logistic Regression Confusion Matrix

<p align="center">
 <img width="700" height="500" src=images/logistic_reg.png>
 </p>

#### Adaboost Confusion Matrix

<p align="center">
 <img width="700" height="500" src=images/adaboost_cm.png>
 </p>

## Repository Structure

```
├── data
├── images
├── Final_notebook.ipynb
├── Pump_it_up_Data_Mining_the_Water_Crisis.pdf
└── README.md
```


