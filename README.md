# Fraud-Detection-ML

# Project Overview:
This project aims to develop a machine learning system for high-accuracy fraud detection using Logistic Regression, Decision Trees, and Neural Networks. The project also includes customer segmentation using K-Means clustering for targeted marketing. The primary dataset contains various transaction details, including payment methods, transaction times, locations, and more.

# Table of Contents:
Project Overview
Data Description
Data Cleaning and Preprocessing
Exploratory Data Analysis (EDA)
Fraud Detection Model
Customer Segmentation
Results and Evaluation
Usage
Dependencies
Authors

# Data Description
The dataset contains transaction details with the following columns:

txn_id: Transaction ID
txn_type: Type of transaction
txn_subtype: Subtype of transaction
initiating_channel_id: Channel ID that initiated the transaction
txn_status: Status of the transaction (e.g., Successful, Failed, On Hold)
payer_psp: Payment Service Provider of the payer
payee_psp: Payment Service Provider of the payee
remitter_bank: Bank of the payer
beneficiary_bank: Bank of the payee
payer_handle: Handle of the payer
payer_app: Application used by the payer
payee_handle: Handle of the payee
payee_app: Application used by the payee
payee_requested_amount: Amount requested by the payee
payee_settlement_amount: Amount settled to the payee
payer_location: Location of the payer
payer_city: City of the payer
payer_state: State of the payer
payee_location: Location of the payee
payee_city: City of the payee
payee_state: State of the payee
payer_os_type: Operating system type of the payer
payee_os_type: Operating system type of the payee
beneficiary_mcc_code: Merchant Category Code of the beneficiary
remitter_mcc_code: Merchant Category Code of the remitter
custref_transaction_ref: Customer reference transaction reference
cred_type: Credit type
cred_subtype: Credit subtype
payer_app_id: Application ID of the payer
payee_app_id: Application ID of the payee
initiation_mode: Mode of initiation
dt_txn_comp: Date of transaction completion
txn_comp_time: Time of transaction completion

# Data Cleaning and Preprocessing
Drop Irrelevant Columns: Columns such as error_code, dt_time_txn_compl, time_of_day, and @dropdown were dropped due to irrelevance or excessive missing values.
Handle Missing Values: Missing values were filled with the mode for simplicity.
Feature Engineering:
Converted dt_txn_comp to datetime format.
Extracted year, month, day, weekday, and hour from the dt_txn_comp and txn_comp_time columns.
Define Target Variable: Created is_fraud where transactions with status 'Successful' are labeled as 0 (non-fraud) and others as 1 (fraud).

# Exploratory Data Analysis (EDA)
Analyzed patterns in fraudulent transactions:
Top cities with fraudulent transactions: Munger, Udhampur, Pali, Barasat, Sambalpur, Chittoor, Nanded, Hisar, Vasco da Gama, Bathinda.
Top payment methods with fraudulent transactions: Credit Card, Home Loan, Debit Card, Overdraft, Line of Credit, Auto Loan, Personal Loan.
Fraudulent transactions by hour: Peaks at hours 0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22.
Top credit subtypes with fraudulent transactions: Secured Credit Card, Prepaid Debit Card, Business Overdraft, Fixed-Rate Mortgage, Adjustable-Rate Mortgage (ARM), Balance Transfer Credit Card, Personal Overdraft, Personal Line of Credit, New Car Loan, Rewards Credit Card.

# Fraud Detection Model
Feature Encoding and Scaling:
One-hot encoded categorical variables.
Scaled numerical features using StandardScaler.
Model Training:
Split the data into training and testing sets.
Trained a Logistic Regression model using a pipeline with preprocessing steps.
Prediction Function: Developed a function to predict fraud for new transactions using the trained model.

# Customer Segmentation
Feature Selection: Selected relevant features for clustering (e.g., payer_city, payee_city, payee_requested_amount, hour, cred_type, cred_subtype).
Encoding and Scaling: One-hot encoded categorical variables and scaled numerical features.
K-Means Clustering:
Used the Elbow Method to determine the optimal number of clusters.
Applied K-Means clustering with the optimal number of clusters.
Cluster Analysis: Analyzed and described the characteristics of each cluster.

# Results and Evaluation
Fraud Detection:
Classification report, confusion matrix, and ROC-AUC score used to evaluate the model.
The prediction function was tested with various transactions to ensure accuracy.
Customer Segmentation:
Clusters were visualized using PCA components.
Each cluster was analyzed to determine customer characteristics for targeted marketing.

# Usage
To use this project, follow these steps:
git clone <repository-url>
cd <repository-directory>

pip install -r requirements.txt

jupyter notebook

# Dependencies
Python 3.10
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter

# Authors
Shashwat Dixit
shashwat.dixit1002@gmail.com
