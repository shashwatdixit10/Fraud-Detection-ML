Fraud-Detection-ML

Project Overview:
This project aims to develop a machine learning system for high-accuracy fraud detection using Logistic Regression, Decision Trees, and Neural Networks. The project also includes customer segmentation using K-Means clustering for targeted marketing. The primary dataset contains various transaction details, including payment methods, transaction times, locations, and more.

Table of Contents:
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

Data Description
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

