DABA Day 2 – Supply Chain Delay Prediction and Contract Compliance
Project Overview

This project is developed as part of DABA (Data Analytics and Business Analytics) Day 2.

The project focuses on developing a machine learning model to predict supply-chain shipment delays and defining a contract-compliance workflow to evaluate vendor contracts.

The system combines shipping data, machine learning, vendor information, and contract compliance analysis to identify potential supply-chain risks.

Problem Statement

Supply-chain delays can affect delivery schedules, customer satisfaction, inventory planning, and overall business operations.

At the same time, vendors are required to follow contractual conditions such as delivery periods, delay notification requirements, insurance, confidentiality, and termination clauses.

This project addresses both problems by:

Predicting whether a shipment may be delayed.
Identifying vendors associated with potential delays.
Checking important contract-compliance requirements.
Calculating vendor compliance scores.
Combining delay prediction and contract compliance to determine an overall risk level.
Objectives
Develop a machine learning model for supply-chain delay prediction.
Generate and analyze logistics tracking data.
Identify important factors associated with shipment delays.
Create a vendor contract database.
Define a contract-compliance checking workflow.
Calculate vendor compliance scores.
Combine shipment predictions with contract compliance.
Generate an overall vendor risk classification.
Export the final analysis as a CSV file.
Technologies Used
Python
Google Colab
Pandas
NumPy
Scikit-learn
Random Forest Classifier
Matplotlib
Seaborn
CSV datasets
GitHub
Dataset

Two datasets are used in this project.

1. Shipping Dataset

The shipping dataset contains 500 randomly generated shipment records.

The main attributes are:

Column	Description
Shipment_ID	Unique shipment identifier
Vendor	Vendor responsible for shipment
Origin	Shipment origin
Destination	Shipment destination
Shipping_Mode	Road, Rail, Air, or Sea
Distance_km	Shipping distance
Weather	Weather condition
Traffic	Traffic condition
Planned_Delivery_Days	Expected delivery duration
Actual_Delivery_Days	Actual delivery duration
Delay_Days	Number of delayed days
Delayed	Delay indicator
2. Vendor Contract Dataset

The vendor contract dataset contains contract-related information for vendors.

Important fields include:

Delivery period
Payment period
Delay notification requirement
Insurance
Confidentiality
Termination clause
Compliance score
Compliance status
Project Workflow
Shipping Data
      |
      v
Data Preprocessing
      |
      v
Feature Selection
      |
      v
Random Forest Classifier
      |
      v
Delay Prediction
      |
      v
Vendor Identification
      |
      v
Vendor Contract Database
      |
      v
Contract Compliance Checking
      |
      v
Compliance Score
      |
      v
Overall Vendor Risk
      |
      v
Final Report
Methodology
Step 1 – Generate Shipping Data

A random logistics dataset containing 500 shipment records is generated.

The dataset contains different:

Vendors
Origins
Destinations
Shipping modes
Weather conditions
Traffic conditions
Distances
Planned delivery durations
Step 2 – Data Preprocessing

The dataset is checked for:

Missing values
Duplicate records
Data distribution
Numerical and categorical features

Categorical variables are converted into machine-readable features using One-Hot Encoding.

Step 3 – Feature Selection

The following features are used for prediction:

Vendor
Origin
Destination
Shipping_Mode
Distance_km
Weather
Traffic
Planned_Delivery_Days

The target variable is:

Delayed

Actual_Delivery_Days and Delay_Days are not used as prediction inputs because they are known only after delivery and could cause data leakage.

Step 4 – Machine Learning Model

A Random Forest Classifier is used to predict shipment delays.

The dataset is divided into:

80% training data
20% testing data

The model predicts two classes:

0 → On Time
1 → Delayed
Step 5 – Model Evaluation

The model is evaluated using:

Accuracy
Precision
Recall
F1-score
Confusion Matrix
Step 6 – Delay Probability

The model also generates a delay probability for each shipment.

This helps identify shipments that may require additional monitoring.

Step 7 – Contract Compliance

A vendor contract database is created containing important contractual requirements.

The workflow checks:

Insurance
Confidentiality
Termination Clause

Each vendor receives a compliance score based on the required clauses.

Compliance Classification
100%       → Compliant
66%–99%    → Partially Compliant
Below 66%  → Non-Compliant
Step 8 – Vendor Risk Analysis

The predicted shipment delay information is combined with contract compliance information.

The resulting risk categories are:

Low Risk
Medium Risk
High Risk

The risk classification is based on the combination of predicted shipment delays and contract compliance status.

Final Output

The final output contains:

Field	Description
Vendor	Vendor name
Shipment_Count	Number of tested shipments
Predicted_Status	Predicted shipment status
Average_Delay_Probability	Average probability of delay
Compliance_Score	Contract compliance percentage
Compliance_Status	Contract compliance classification
Overall_Risk	Combined vendor risk level
Project Output

The project produces:

Shipment delay predictions
Delay probabilities
Confusion matrix
Vendor delay analysis
Contract compliance scores
Vendor compliance status
Overall vendor risk analysis
Final CSV report
Repository Structure
DABA-Day-2-Supply-Chain-Delay-Prediction/
│
├── README.md
├── DABA_Day_2_Supply_Chain.ipynb
│
├── data/
│   ├── shipping_data.csv
│   └── vendor_contracts.csv
│
├── output/
│   └── DABA_Day2_Final_Output.csv
│
├── screenshots/
│   ├── dataset.png
│   ├── model_accuracy.png
│   ├── confusion_matrix.png
│   ├── delay_prediction.png
│   ├── contract_compliance.png
│   └── final_output.png
│
└── requirements.txt
Key Learning Outcomes

Through this project, the following concepts were implemented:

Data generation
Data preprocessing
Exploratory data analysis
Categorical feature encoding
Machine learning classification
Random Forest
Model evaluation
Prediction probability
Contract compliance analysis
Vendor risk analysis
Data visualization
CSV report generation
Future Enhancements

The project can be extended by:

Using real-time logistics tracking data.
Connecting with APIs for weather and traffic information.
Using real procurement contracts instead of sample contract data.
Implementing NLP for automatic contract clause extraction.
Adding a Streamlit dashboard.
Adding real-time vendor monitoring.
Sending automated alerts for high-risk shipments.
Using advanced NLP or Large Language Models for contract analysis.
Conclusion

This project demonstrates how Data Analytics, Machine Learning, and Business Analytics can be combined to improve supply-chain monitoring.

The system predicts potential shipment delays, evaluates vendor contract compliance, and combines both analyses to provide a structured view of vendor risk.

It provides a foundation
