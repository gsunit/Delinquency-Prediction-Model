# Delinquincy Prediction Model
Delinquency is a condition that arises when an activity or situation does not occur at its scheduled (or expected) date i.e., it occurs later than expected.

## Problem Statement
Create a delinquency model which can predict in terms of a probability for each loan transaction, whether the customer will be paying back the loaned amount within 5 days of insurance of loan (Label ‘1’ & ’0’)

## Model
 - We used various permutations of the following models
     - Random Forest Classifier
     - XGBoost
 - The training data was highly skewed, so we tried various resampling methods
     - Oversampling of majority class
     - Downsampling of minority class
     - SMOTE
 - We also used Recursive Feature Elimination (RFE) to extract only the relavant features to train the model on
 - Among the models the one with the highest accuracy (90.58%) was the following
     - Random Forest Classifier, Downsampling Minority, RFE with 7 features extracted
 - Although, upon analyzing the complete classification report we find that the model doesn't generalize well to the minority class.
 - The recall values for all the models for the `negative (false/0)` case is pretty low.
 - This clearly indicates there is a need to improve the performance of the model
 - Given more time, I would probably try out a few more classifiers, tune the hyperparameters and attempt to generate more useful features through feature engineering.
 - However for now, this is what I could come up with in a couple of days! :)
