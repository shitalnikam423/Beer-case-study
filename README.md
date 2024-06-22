# Beer-case-study
Overview
This repository contains a data science case study focused on predicting the overall rating of beers using a dataset of beer reviews. The dataset includes various attributes related to the beers, reviews, and reviewers. The goal is to build and evaluate machine learning models to predict the overall rating of beers, with a detailed explanation of the steps taken and the results obtained.

Dataset
The dataset train.csv contains the following columns:

index: An identifier for the review
beer/ABV: The alcohol by volume of the beer
beer/beerId: A unique ID indicating the beer reviewed
beer/brewerId: A unique ID indicating the brewery
beer/name: Name of the beer
beer/style: Style of the beer
review/appearance: Rating of the beer's appearance (1.0 to 5.0)
review/aroma: Rating of the beer's aroma (1.0 to 5.0)
review/overall: Rating of the beer overall (1.0 to 5.0)
review/palate: Rating of the beer's palate (1.0 to 5.0)
review/taste: Rating of the beer's taste (1.0 to 5.0)
review/text: The text of the review
review/timeStruct: A dict specifying when the review was submitted
review/timeUnix: Unix timestamp of the review
user/ageInSeconds: Age of the user in seconds
user/birthdayRaw: Raw birthday of the user
user/birthdayUnix: Unix timestamp of the user's birthday
user/gender: Gender of the user (if specified)
user/profileName: Profile name of the user

Objective
The objective is to predict the review/overall rating of the beer using various features from the dataset. This involves data cleaning, feature engineering, model training, and evaluation.

Steps
Data Loading and Initial Inspection: Load the dataset and inspect for missing values and data types.

Data Cleaning: Handle missing values, convert date columns to datetime, and extract meaningful features from date columns.
Feature Engineering: Encode categorical variables, extract features from text columns using TF-IDF, perform sentiment analysis on text data, and normalize numerical features.

Data Splitting: Split the dataset into training and testing sets.
Model Training and Evaluation: Train multiple models and evaluate them using metrics such as MSE, MAE, and R2.
Results Interpretation: Compare the performance of different models and select the best-performing one.

Results
The following models were trained and evaluated:

Linear Regression:

MSE: 0.1615581857700098
MAE: 0.3061381916727922
R2: 0.6805186699937869
Random Forest:

MSE: 0.16434218
MAE: 0.30928
R2: 0.6750133210999024
Gradient Boosting:

MSE: 0.15827979084548163
MAE: 0.3032601296520881
R2: 0.6870016963151204
HistGradient Boosting:

MSE: 0.15743848809398764
MAE: 0.30249589054892717
R2: 0.6886653725980902

Conclusion:
HistGradient Boosting performed the best with the lowest MSE and MAE, and the highest R2.
Gradient Boosting also performed well, closely following HistGradient Boosting.
Linear Regression and Random Forest had slightly lower performance but were still competitive.
 
