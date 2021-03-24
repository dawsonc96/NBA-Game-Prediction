# NBA Game Prediction
Predicting the outcome of any given NBA game


## Overview
As the sport of basketball has becoming increasingly popular, data has come to the forefront for analyzing player and team performance. NBA owners will do anything to garner an advantage over their opponents,  and players look to managers and coaches to help them improve through insight on relevant data. 

Bettors also look to statistics to better inform themselves of what the potential outcome of a game may be. Using NBA statistics from basektball-reference.com over the past 18 years, we created a model to predict whether the home team would win a given match based on their previous statistics. We use strictly Team data in eeach model.

## Business Problem
Mark Cuban, owner of the Dallas Mavericks, has been contemplating hiring and outside analytics consultant as his team has been on quite a long losing streak. Cuban doesn't know what is going wrong and is hoping someone with a strong analytics background can help him understand their teams issues. Several outside consultants are pitching to him and we are one of them! We decided to create a model to help predict why any given NBA team may win a game to help him understand why his team may be losing.

## Data

To understand the NBA as a whole, we decided to do some league research and exploratory analysis to better understand the data we are analyzing. Developing our domain knowledge was important in order to be able to succinctly analyze our data. Using basketball-reference.com as our datasource, we obtained game data for each team over the past 18 years (over 23,000 observations). Before featurn engineering, our data had over 70 columns (features) of information relating to a specific game played.

## Methods

### Cleaning and Feature Engineering

This project uses data cleaning and feature engineering. Cleaning our data was important in order to analyze it. Many of the win-loss records of each team were in the wrong data type (strings) and needed to be converted in order to use them within our model. Almost all features in our model were engineered and not taken directly from our sourced data. We engineered features that showed the last ten games a team had played and average those stats out in order to predict how they would play in an upcoming game. We also created a feature that show the disparity between two teams, which significantly helped our model. Cleaning our data and building these features helped make our model more interpretable and significant.


