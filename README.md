# deep-learning-challenge
Module 21 Challenge

## Overview of the Analysis

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. The purpose of this analysis is to utilize machine learning and neural networks with the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Results

* Machine Learning Model 1:
  * Data Preprocessing:
     * Target variable: IS_SUCCESSFUL
     * Features: APPLICATION_TYPE (binned > 500), AFFILIATION, CLASSIFICATION (binned > 1000), USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
     * Variables removed: EIN, NAME

  * Compiling, Training, Evaluating:
     * 2 hidden layers using relu and 43 neurons each
     * 50 epochs
     * Loss: 55.31%, Accuracy: 72.89%
     * Target model performance was not reached
     * The following steps were taken in attempt to increase model performance in model #2:
         1. Increase number of hidden layers and neurons
         2. Change split between bins on APPLICATION_TYPE
         3. Remove ASK_AMT from features 

* Machine Learning Model 2:
  * Data Preprocessing:
     * Target variable: IS_SUCCESSFUL
     * Features: APPLICATION_TYPE (binned > 1000), AFFILIATION, CLASSIFICATION (binned > 1000), USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS
     * Variables removed: EIN, NAME, ASK_AMT

  * Compiling, Training, Evaluating:
     * 5 hidden layers using relu and 100 neurons each
     * 50 epochs
     * Loss: 56.90%, Accuracy: 72.89%
     * Target model performance was not reached

## Summary

Overall, both models performed below the target performance level. Possible ways to continue improving the accuracy of the model would be using different activation functions for the hidden layers, changing bin sizes and adding more bins for feature variables, and adding back in/binnning the ASK_AMT column.
