# AIr-Yards-Buy-Low
Based on Josh Hermsmeyer's Air Yards Buy Low Model


The Air Yards Buy Low model was a concept originally created by Josh Hermsmeyer. The concept is that wide receiver scoring is not linear through the year, but rather cycles through peaks and valleys. We can predict players that will outperform their expectation in a given week by using regression analysis to predict the expected points a player should have based on Targets per Game (quantity of opportunity) and Depth of Target (quality of opportunity). There are additional datapoints that can be considered when evaluating player under or over performance such as red zone/end zone targets, but for simplicity this regression analysis uses only two features.

A previous iteration of this model used data from Josh's website, Airyards.com, but support for the site appears to be deprecated so all of the data comes from Pro-Football-Reference.com. The model uses 2018 data as a training set, and 2019 as a test set. The Airyards iteration used data from 2011-2016 as training, 2017 as validation, and 2018 as test. Unfortunately pro-football-reference does not have this level of historical data.

The regression is a non-linear SVR. In the airyards model this proved to be the most accurate version. The use of a non-linear model is to account for consistent errors at the tails. 
