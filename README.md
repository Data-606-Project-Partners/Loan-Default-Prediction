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

Dataset column interpretations: (selection of important columns provided here)
> - col1
> - col2
> - ...


### Project Methodology:

### Project 
