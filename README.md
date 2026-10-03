SWYNEX — Hotel Booking Exploratory Data Analysis
Project Overview

This project was completed as part of my Data Analysis / Data Engineering Internship at SWYNEX Technologies.

The objective of this project is to perform Exploratory Data Analysis (EDA) on a prepared hotel booking dataset and identify meaningful patterns, relationships, and insights that can support business understanding and future predictive modeling.

The analysis focuses mainly on hotel booking cancellations and the factors associated with different cancellation patterns.

Objectives
Explore the prepared hotel booking dataset.
Understand the structure and characteristics of the data.
Analyze hotel booking cancellations.
Answer business-oriented questions using data.
Perform statistical analysis.
Create meaningful visualizations.
Identify important patterns and insights.
Identify potential features for future cancellation prediction.
Business Context

Hotel cancellations can affect room availability, revenue planning, and hotel operations.

This analysis investigates:

What percentage of bookings are cancelled?
Do cancellation rates differ by hotel type?
Does booking lead time relate to cancellation?
Does deposit type relate to cancellation?
Do different market segments have different cancellation rates?

Note: EDA identifies patterns and associations in the dataset. It does not establish causal relationships.

Dataset

The project uses a public Hotel Booking Demand dataset.

The prepared dataset contains:

87,396 records
33 columns

The dataset includes information related to hotel type, cancellation status, lead time, arrival information, length of stay, customer type, market segment, deposit type, guest information, ADR, and reservation status.

Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook
Git & GitHub
EDA Workflow
Prepared Dataset
       ↓
Load Dataset
       ↓
Dataset Overview
       ↓
Descriptive Statistics
       ↓
Business Questions
       ↓
Statistical Analysis
       ↓
Visualizations
       ↓
Key Findings
       ↓
Model / Decision Relevance
       ↓
Conclusion
Business Questions & Answers
1. What percentage of hotel bookings were cancelled?

Answer:
The dataset contains 87,396 bookings, of which 24,025 were cancelled.

The overall cancellation rate was 27.49%.

This means more than one-quarter of the recorded bookings were cancelled.

2. Do City Hotels and Resort Hotels have different cancellation rates?
Hotel Type	Cancellation Rate
City Hotel	30.04%
Resort Hotel	23.48%

Answer:
Yes. City Hotel bookings had a 30.04% cancellation rate, while Resort Hotel bookings had a 23.48% cancellation rate.

The difference was 6.56 percentage points.

hotel can therefore be considered a candidate feature for future cancellation prediction.

3. Does booking lead time relate to cancellation?
Booking Lead Time	Cancellation Rate
0–7 days	8.43%
8–30 days	25.37%
31–90 days	32.01%
91–180 days	34.98%
181+ days	39.74%

Answer:
Cancellation rates increased as booking lead time increased in this dataset.

The cancellation rate increased from 8.43% for bookings made 0–7 days before arrival to 39.74% for bookings made 181+ days before arrival.

lead_time can be considered a candidate feature for future cancellation prediction.

4. Does deposit type relate to cancellation?
Deposit Type	Cancellation Rate
No Deposit	26.68%
Non Refund	94.70%
Refundable	24.30%

Answer:
Yes. Cancellation rates varied substantially by deposit type.

Non Refund bookings had a 94.70% cancellation rate, compared with 26.68% for No Deposit and 24.30% for Refundable bookings.

deposit_type can be considered an important candidate feature for future cancellation prediction.

Note: This is an observed association in the dataset and does not prove that deposit type causes cancellations.

5. Do different market segments have different cancellation rates?
Market Segment	Cancellation Rate
Aviation	19.82%
Complementary	12.54%
Corporate	12.11%
Direct	14.72%
Groups	27.01%
Offline TA/TO	14.85%
Online TA	35.35%
Undefined	100.00%

Answer:
Yes. Cancellation rates varied across market segments.

Online TA bookings had a 35.35% cancellation rate, while Corporate bookings had a 12.11% cancellation rate.

The Undefined category showed a 100% cancellation rate, but this result should be interpreted carefully based on its booking volume.

market_segment can be considered a candidate feature for future cancellation prediction.

Key Insights
The overall cancellation rate was 27.49%.
City Hotel had a higher cancellation rate (30.04%) than Resort Hotel (23.48%).
Cancellation rates increased with longer booking lead times.
Deposit type showed substantial differences in cancellation rates.
Market segment showed different cancellation patterns.
hotel, lead_time, deposit_type, and market_segment can be considered potential candidate features for future cancellation prediction.
Model & Decision Relevance

The EDA identified several variables that may be useful for a future hotel booking cancellation prediction model:

hotel
lead_time
deposit_type
market_segment

A potential future workflow would be:

EDA
 ↓
Feature Engineering
 ↓
Feature Selection
 ↓
Train/Test Split
 ↓
Model Training
 ↓
Model Evaluation
 ↓
Prediction

This project focuses on Exploratory Data Analysis and does not include machine learning model training or evaluation.

Visualizations

The project includes visualizations for:

Overall booking cancellation status
Cancellation rate by hotel type
Cancellation rate by booking lead time
Cancellation rate by deposit type
Cancellation rate by market segment
Project Structure
SWYNEX-Exploratory-Data-Analysis/
│
├── data/
│   └── hotel_bookings_cleaned.csv
│
├── Notebook/
│   └── 02_exploratory_data_analysis.ipynb
│
├── output/
│   └── visualizations/
│
├── README.md
│
└── requirements.txt
How to Run
git clone https://github.com/Anny91/SWYNEX-Exploratory-Data-Analysis.git
cd SWYNEX-Exploratory-Data-Analysis
pip install -r requirements.txt
jupyter notebook

Open:

Notebook/02_exploratory_data_analysis.ipynb

Run the notebook cells from top to bottom.

Limitations
The analysis is based on the available historical dataset.
EDA identifies patterns and associations but does not establish causation.
Categories with very small numbers of records can produce extreme percentages.
This project does not include machine learning model training or evaluation.
Further feature engineering and validation would be required before using these findings in a production environment.
Previous Task

This project builds on the previous SWYNEX Hotel Data Preparation task.

Previous Repository:
https://github.com/Anny91/SWYNEX-Hotel-Data-Preparation

Author
Aniket Sharma

Aspiring Data Engineer

Skills Demonstrated
Python
SQL
Pandas
NumPy
Data Cleaning
Exploratory Data Analysis
Data Visualization
Business Analysis
Git & GitHub
Conclusion

This project demonstrates an Exploratory Data Analysis workflow on a prepared hotel booking dataset.

The analysis identified meaningful differences in cancellation behavior across hotel types, booking lead times, deposit types, and market segments.

These findings provide a foundation for further feature engineering and predictive modeling.

The project strengthened practical skills in Python, Pandas, statistical analysis, data visualization, business-question-driven analysis, and GitHub project documentation.
