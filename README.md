# Airline-Passenger-Referral-Prediction
## Problem Statement

Data includes airline reviews from 2006 to 2019 for popular airlines around the world with multiple choice and free text questions. Data is scraped in Spring 2019. The main objective is to predict whether passengers will refer the airline to their friends.

Feature descriptions briefly as follows:

* airline: Name of the airline.
* overall: Overall point is given to the trip between 1 to 10.
* author: Author of the trip
* reviewdate: Date of the Review customer review: Review of the customers in free text format
* aircraft: Type of the aircraft
* travellertype: Type of traveler (e.g. business, leisure)
* cabin: Cabin at the flight date flown: Flight date
* seatcomfort: Rated between 1-5
* cabin service: Rated between 1-5
* foodbev: Rated between 1-5 entertainment: Rated between 1-5
* groundservice: Rated between 1-5
* valueformoney: Rated between 1-5
* recommended: Binary, target variable.

![image](https://user-images.githubusercontent.com/85817763/179201903-4c94d998-0caf-47b4-b2cb-200aae435a8a.png)

## Project Approach
This is basically a classification (binary classification) problem statement as the target variable (dependent variable) is categorical in nature.
So, following are the steps taken in whole analysis process:
* Got an overview of the dataset in order to know the nature of the dataset.
* Inspected the data so as to make sure that the dataset contains any null, missing and duplicates value.
* Lots of missing and null values were detected, so performed data cleaning and pre-processing.
* Removed less important features and rest features with missing and null values are treated by substituting categorical missing values with mode value of the feature     and continuous missing values with the median values (Have not used mean as mean values are influenced by outliers).
* Performed exploratory data analysis so as to extract some fruitful insights which may help solving some business problems.
* Splitted dataset into training and testing dataset (75% of the dataset is used for training & 25% of the dataset is used for testing).
* Created some machine learning models to predict the target class. Machine learning algorithms taken in use are as follows:
  1. Logistic Regression
  2. Random Forest 
  3. Decision tree
  4. KNN
* Performed hyperparameter tuning of 'Random Forest' and 'KNN' using GridSearchCV so as to fine tune the model in order to get better accuracy.
* Compared model performance on the basis of evalution metrics to spot the best performing model.

## Machine Leaning Models

➡️ **Logistic Regression**

Following is the confusion matrix for logistic regression model:

![image](https://user-images.githubusercontent.com/85817763/179205797-935ba7a3-1997-450c-97be-10e8767d84c5.png)

Accuracy of the model : **93.9024 %**

➡️ **Random Forest**

Following is the confusion matrix for random forest model:

![image](https://user-images.githubusercontent.com/85817763/179205996-87f3c530-0db1-4660-a1d2-240132835c53.png)

Accuracy of the model : **93.7507 %**

➡️ **Decision Tree**

Following is the confusion matrix for decision tree model:

![image](https://user-images.githubusercontent.com/85817763/179206565-85b9836c-e134-4d5a-aea4-b0b2c29656d9.png)

Accuracy of the model : **92.2153 %**

➡️ **KNN**

Following is the confusion matrix for KNN model:

![image](https://user-images.githubusercontent.com/85817763/179206826-91da5142-79f7-42ef-98f0-ef5760e824c1.png)

Accuracy of the model : **93.5991 %**

➡️ **Random Forest (GridSearchCV)**

Following is the confusion matrix for random forest model after performing hyperparameter tuning:

![image](https://user-images.githubusercontent.com/85817763/179207115-5060b0ee-3640-4ac5-92ac-f3aefc777db0.png)

Accuracy of the model : **94.0161 %**

➡️ **KNN(GridSearchCV)**

Following is the confusion matrix for KNN model after performing hyperparameter tuning:

![image](https://user-images.githubusercontent.com/85817763/179207370-b0a132a1-5be0-46e4-8d0a-d6632ce492f2.png)

Accuracy of the model : **93.9529 %**

## Metrics Comparison

All the models are evaluated and compared on metrics mentioned below:

![image](https://user-images.githubusercontent.com/85817763/179207721-e9e79b97-4d1c-43c1-84ae-0b9d5062a750.png)

## Conclusions

*   "Solo Leisure" has the highest ratings among all traveller type category.
*   "Solo Leisure" has been the most value for money.
*   77% of the passengers are economy class traveller.
*   Economy class has most recommendations.
*   Passengers seems dissatisfied as most of them rated 1 out of 10 in overall rating. 
*   'American Airlines' has maximum number of trips.
*   'NO' responses are more compared to 'YES' responses.
*   Four machine learning models have been implemented (KNN, Random Forest, Descision Tree, Logistic Regression).
*   GridSearchCV used for the purpose of hyperparameter tuning.
*   'Accuracy', 'Recall', 'Precision', 'F1-score' & 'ROC-AUC-SCORE' are the evaluation metrics taken into consideration.
*   Random Forest after hyperparameter tuning performed the best out of all models.
*   Decision Tree performed the worst.
