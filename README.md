Credit Card Fraud Detection Analysis (Power BI Project)


📌 Project Overview
"First, I acquired the dataset titled 'Credit Card Fraud Detection Analysis', from Kaggle." 
And Now This project focuses on analyzing credit card transaction data to identify fraud patterns using Power BI. The goal is to uncover insights related to fraudulent activities based on transaction behavior, location, time, and transaction types.


🎯 Objectives

Identify fraudulent transactions in the dataset

Analyze fraud patterns based on time, location, and transaction type

Calculate key performance indicators (KPIs)

Build an interactive Power BI dashboard for visualization


📂 Dataset Information

The dataset contains transaction-level data with the following key columns:

Transaction ID

Transaction Date

Transaction Amount

Merchant ID

Transaction Type

Location

Fraud Indicator (0 = Non-Fraud, 1 = Fraud)


🧹 Data Cleaning (Power Query)

Performed data cleaning using Power Query Editor:

Converted TransactionDate to Date/Time format

Changed Amount to Decimal Number

Converted IsFraud to Whole Number

Removed duplicate transactions using TransactionID

Handled missing/null values

Validated data quality using column profiling


⚙️ Feature Engineering

Created new columns using DAX for time-based analysis:

Month Column

Month = MONTH('credit_card_fraud_dataset'[TransactionDate])

Day Column

Day = FORMAT('credit_card_fraud_dataset'[TransactionDate], "dddd")

Hour Column

Hour = HOUR('credit_card_fraud_dataset'[TransactionDate])

These features helped analyze fraud patterns across different time intervals.


📊 Key Metrics (DAX Measures)

Developed important KPIs using DAX:

Total Transactions

Total Transactions = COUNT(credit_card_fraud_dataset[TransactionID])

Total Fraud Transactions

Total Fraud = SUM(credit_card_fraud_dataset[IsFraud])

Fraud Rate (%)

Fraud Rate = DIVIDE(SUM(credit_card_fraud_dataset[IsFraud]), COUNT(Fraud[TransactionID]))

Total Transaction Amount

Total Amount = SUM(credit_card_fraud_dataset[Amount])


📈 Data Analysis & Visualizations
1. Fraud by Location

Bar chart showing fraud distribution across different locations

2. Fraud by Transaction Type

Pie chart comparing fraud across transaction types (Online, POS, ATM)

3. Fraud Trend by Month

Line chart showing monthly fraud trends

4. Fraud by Hour

Column chart identifying peak hours of fraudulent activity

5. High-Risk Analysis

Identified high-risk locations and transaction types

Analyzed fraud patterns during late-night hours


📊 Dashboard Features

KPI cards for quick insights:

Total Transactions

Total Fraud Transactions

Fraud Rate (%)

Total Transaction Amount

Interactive slicers:

Location

Transaction Type

Month

User-friendly and interactive dashboard design


🔍 Key Insights

Fraud transactions are more frequent in specific locations

Online transactions show higher fraud rates compared to others

Fraud activity peaks during late-night hours

High-value transactions are more likely to be fraudulent


🛠 Tools & Technologies Used

Power BI

Power Query

DAX (Data Analysis Expressions)


🚀 Conclusion

This project demonstrates how Power BI can be used to analyze transaction data and detect fraud patterns effectively. It highlights the importance of data cleaning, feature engineering, and visualization in real-world data analytics projects.







