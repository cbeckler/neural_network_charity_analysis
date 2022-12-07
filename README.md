# neural_network_charity_analysis

## Overview

The analyst was asked to create a deep learning neural network model to predict whether or not applicants to charity funding would be successful. After creating an initial model with lower than desired accuracy, the analyst explored different iterations of the model to determine whether or not a deep learning neural network would be a good solution to the organization's request.

## Results

The analyst will discuss the first optimized model, which was the only one to have improvement over the initial model.

### Data Preprocessing

* The target variable of the model was the binary IS_SUCCESSFUL variable.
* The feature variables of the model were APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.
* The variables EIN and NAME were discarded.

### Compiling, Training, and Evaluating the Model

* The model had 2 layers, as a deep learning model can have greater capability to catch complexities in data than single layer neural networks, and the model performed better with 2 layers than 3. 
* The first layer had 120 nodes, roughly 3 times the amount of features being input into the model, versus the initial model's doubling of nodes. The second layer had 45, which was scaled to increase from the initial 30 nodes by the same ratio that the first layer increased. 
* The hidden layers had the relu function applied for activation, as the data was largely positive and nonlinear. The output layer used sigmoid activation as the desired classification is binary.
* The model did not achieve target performance, with an accuracy of only 0.60--only slightly better than chance performance.
* With this and the other iterations, a few different steps were taken to try to increase model performance over the initial model:
1) Increase nodes (only marginally successful)
2) Increase layers (decreased model performance)
3) Remove USE_CASE and SPECIAL_CONSIDERATIONS as features (decreased model performance)

## Summary

Overall, this model did not solve the issue of classifying charity funding applicants as likely to be successful or unsuccesful. The accuracy of the best iteration was only slighly better than chance. The analyst recommends trying a logistic regression model, which may be able to provide similar or superior performance while being much less computationally-intensive. It may be that this classic model type can more effectively classify the data. Despite being much simpler, logisitic regression models have a long history of being validated for business use, and exploring its capabilities would likely be a good step forward for this project.


