# Loan-Default-Prediction

### Link to Deploy:
https://loan-maximization-webapp.onrender.com/

> Note:  Large loans that result in defaults take a long time to calculate.  Please be patient.

Much thanks to the tutorials:
- https://www.youtube.com/watch?v=jQjjqEjZK58
- https://www.youtube.com/watch?v=QKcVjdLEX_s


### Project Background:
When banks are choosing who is allowed to receive a loan, banks are often forced to predict whether or not to trust that an individual will default on his loan or be able to pay it back in full.  In efforts to prevent their losses, banks have developed strategies for mitigating their own risk, such as credit ratings, FICO scores, and analysis of the debt-to-income ratio.  Significant research has gone into creating methods of classifying potential loan candidates into either of the two categories "loan" or "defaulting", but often overlooked is the opportunity to gauge what limit a risky individual can afford before the default occurs.  

This project hopes to create an algorithm that will allow users to input certain identifying factors and **(1) determine whether an individual should be considered safe from default**, or **(2) determine what the maximum amount of credit he/she could receive before being unable to return the full quantity of the loan**.  If something similar were applied professionally, it might allow banks to capitalize on opportunities for loans that might otherwise be ignored due to the investment being too risky.

### Project Purpose:
Create a model that will illustrate: \
(1) whether a loaning account will default, \
(2) what conditions will cause that default to occur, \
(3) and how much money the bank will have recouped from the lendee before default.

## Team Members:
Adam Raabe |
Pranav Tanaji Ghadge |
Vishnu Vardhan Reddy Putha.

### Role of Team Members:
Adam Raabe:  Researcher and  Literature Reviewer \
Pranav Tanaji Ghadge: Data Cleansing and Transformation \
Vishnu Vardhan Reddy Putha: Github organizer and Exploratory Data Analysis (EDA)

# Project Data Source:
https://www.kaggle.com/datasets/devanshi23/loan-data-2007-2014?resource=download

### Dataset Specs:
 - Number of Columns: 75
 - Number of Rows: 466,000
 - Target Column: "Loan Status"
 - Target column values:
   - [_Current_] <-- (Left out because these data have not resolved into their final states)
   - Fully Paid
   - **Charged Off**  <-- (For our purposes, equivalent to default)
   - Late (16-30 days)
   - Late (31-120 Days)
   - In Grace Period
 - Original source: Lending Club Data from 2007-2014 (Lending Club is no longer providing this sort of information publically)

 ## Project Methodology:
 ### Data Cleaning: 
    The dataset underwent cleaning procedures to remove unnecessary columns, handle missing values, and convert data types.
 ### Exploratory Data Analysis (EDA):
    Exploratory analysis was conducted to understand the distribution of loan attributes, identify patterns, and explore relationships        between variables. Visualizations were utilized to gain insights into the data.
 ### Model Development:
    Several machine learning models were trained and evaluated using the cleaned dataset to predict loan outcomes. Models include             Logistic Regression, Decision Trees, Random Forest, Support Vector Machines (SVM), Gradient Boosting, and Bagging techniques.
 ### Model Evaluation:
    Model performance metrics such as accuracy, precision, recall, and F1-score were used to evaluate the predictive performance of each      model.
 ### Hyperparameter Tuning: 
    Hyperparameters of selected models were tuned using techniques such as cross-validation to optimize model performance.
 ### Ensemble Learning: 
    Ensemble methods like Voting Classifier and Bagging were employed to combine predictions from multiple models for improved accuracy       and robustness.


 # Project Components:

 ## Data Cleaning and Transformation
  - Removed columns with all-null values and irrelevant columns
  - Merged similar loan status categories
  - Converted date columns to DateTime format
  - Filled missing values with appropriate approximations

 ## Exploratory Data Analysis (EDA)
 The EDA conducted in this project includes:
 
  - Visualizing original distributions of loan amount and annual income
  - Binning continuous variables
  - Analyzing relationships between loan amount, interest rate, and loan grade
  - Examining loan status distribution, purposes, and default rates
  - Exploring correlations between variables and default rates over time
  - Using PCA for dimensionality reduction and visualization

## Model Development and Evaluation
 - Trained and evaluated models including Logistic Regression, Decision Trees, Random Forest, Support Vector Machines (SVM), Gradient     Boosting, and Bagging techniques
 - Used performance metrics such as accuracy, precision, recall, and F1-score for model evaluation
 - Tuned hyperparameters using techniques such as cross-validation to optimize model performance
 - Employed ensemble methods like Voting Classifier and Bagging for improved accuracy and robustness

## Maximizing the Loan Amount Given Default
 ### Method 1 - Stepping Down from a Defaulted Amount until not Default
 - Generated grid and accuracy functions to step downwards from a defaulted loan amount until reaching a likely repayment quantity
 - Utilized linear regression for approximating loss on investment given default
 - Explored other regression models including Random Forest and HistGradientBoostingRegressor for comparison
 - Developed functions for outputting new loan suggestions based on regression model predictions

 ### Method 2 - Linear approximation of Default Quantity, Given Default
 - Crafted a dataset from "only defaults" to estimate the loss on investment
 - Tested linear regression with 1 and 2-dimensional transformations
 - Evaluated other regressors including Random Forest and HistGradientBoostingRegressor for comparison

 ### Results
 - Logistic Regression: Achieved approximately 25% accuracy for predicting "Charged Off" and 86% for "Fully Paid" loans.
 - Decision Trees: Attained around 30% accuracy for predicting "Charged Off" and 88% for "Fully Paid" loans.
 - Random Forest: Achieved about 30% accuracy for predicting "Charged Off" and 89% for "Fully Paid" loans.
 - Support Vector Machines (SVM): Yielded around 25% accuracy for predicting "Charged Off" and 86% for "Fully Paid" loans.
 - Gradient Boosting (XGBoost): Attained approximately 31% accuracy for predicting "Charged Off" and 89% for "Fully Paid" loans.
 - Employed ensemble techniques like Voting Classifier and Bagging for further improvements in accuracy and robustness.
