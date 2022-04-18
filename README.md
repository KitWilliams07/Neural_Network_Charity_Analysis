# Neural_Network_Charity_Analysis

## Overview of the Analysis

The point of this analysis was to use a neural network to create a binary classifier to predict if applications will be successful if funded by Alphabet Soup. That dataset contains more than 34,000 organizations that have recieved funding from Alphabet Soup with various columns highlighting specific features of the fund, in addition to whether it was successful or not. These features will be used to train the neural network and be used to predict the potential success of future funds. 

## Results

Data Preprocessing:

What variable(s) are considered the target(s) for your model?
- The target variable for the model was whether or not the fund was successful or not. There was a column in the dataset labeled 'Is Successful' with a 0 indicating 'No' and a 1 indicating 'Yes'.

What variable(s) are considered to be the features for your model?
- Every other column in the dataset other than the target variable was considered a feature. Only after analyzing the variation of each column did we determine if it would be work as a feature. If the column had a large variance with many outliers it was not used as a feature due to concern it would lead to poor predictions.

What variable(s) are neither targets nor features, and should be removed from the input data?
- The only variable that I removed from the dataset was the "Ask Amount" Variable. 

## Summary 


