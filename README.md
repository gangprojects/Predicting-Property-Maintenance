# Understanding and Predicting compliance in city of Detroit

## Detroit's blight problem

What exactly is blight?

Blight is a term used to signify property or land that is in poor condition due to a lack of upkeep and maintenance. As a result, the property eventually becomes unsafe or uninhabitable.

City of Detroit contains many blighted properties, nearly three-quarters of Detroit residents report their neighborhoods has some blighted properties. Both the state and federal goverment started issuing maintenance fines to owners of blighted properties. 

In reality, there is less than 10% of blight tickets were paid and left astonishing amount of unpaid fines.

##  Introduction

This project aims to solves the unpaid blight fine problem by:

- Predict if the person will comply with the blight ticket fine
- Understand why people failed to comply

If we can study the cause of the unpiad compliance, the Detroit government could understand better how to approach the people responsible for the maintenance of their properties.

## Data Description

- Train 
  - Contains 250,306 rows
  - 34 variables
- Test 
  - 61,001 rows
  - Does not contain out variable of interest: compliance. 
  - Mnay variables are missing in the test compared to train
- Address 
  - Contains each ticket_id's address
- lations
  - contains latitude and longitude coordinates of the address
  
The variable of interest is response compliance which has two category
* 0: Non-compliance
* 1: Compliance

## EDA

We use several plots to analyze the realationship between variables. Some variables such as clean_up_cost, state_fee and admin_fee was all constant among all observation which was dropped in our modelling since it doesnot provide any useful information.

## Data Modelling

Several classification methods was used to fit the training data and validate on the validation set with hyperparameter tuning to find the best performance of each model.
* Logistic regression
* Logistic Regression with over sampling
* Random Forest Classifier
* Gradient Boosting Classifier
* Xtreme Gradient Boosting Classifier
