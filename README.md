# SyriaTel-Customer-Churn-Prediction
<img width="725" height="194" alt="image" src="https://github.com/user-attachments/assets/09683920-1f63-4346-afdd-cc271933c06b" />

Author: Daniel Akwabi

## Overview
Customer churn (the rate at which customers stop doing business with a company) directly impacts revenue, profitability, and long-term growth for telecommunications companies. A spike in churn rates would affect the overall performance of SyriaTel Telecom. By utilizing existing customer information, I will do a forecast on probable exits by customers. In turn, SyriaTel will be in a position to optimize customer retention strategies, maintain customer loyalty, and sustain competitive advantage by establishing the churn trends.

## Business Understanding

### Stakeholders
SyriaTel Telecom

## Business Problem
SyriaTel is experiencing customer churn leading to lost revenue, increased customer acquisition expenses and a reduction in market share. SyriaTel is unable to formulate retention plans due to lack of a clear understanding of customer churn and high-risk customers prediction leading to missed opportunities to improve customer experience, optimize retention, and preserve long-term profitability. This calls for a research on customers who are likely to exit SyriaTel.

To address this, I will develop a data-driven solution that:

- Identifies high-risk customers before they churn.
- Highlights key factors driving attrition.
- Lays out actionable insights to facilitate SyriaTel's implementation of selected retention strategies.

## Data Understanding
This project entails a dataset derived from Kaggle. It includes:

 1.   State     
 2.   Area code                
 3.  Phone number       
 4.  International plan  
 5. Voice mail plan  
 6.   Number vmail messages 
 7.   Churn
 8.   Customer service calls    

- The dataset includes details on customer behavior, usage metrics, and subscription plans, to predict customer churn

## Exploratory Data Analysis

### 1. Distribution of categorical data
<img width="1072" height="424" alt="image" src="https://github.com/user-attachments/assets/63f83715-d844-4302-87a9-6ebc2018b5f4" />

- From this plot, it appears that significantly more customers have no international and voicemail plans.
- We also notice that the number of customers who do not churn is more, which is good for SyriaTel

### 2. Distribution of numerical data
<img width="1072" height="1072" alt="image" src="https://github.com/user-attachments/assets/f3f0fdd3-862a-49c3-8431-f23a8737aa3e" />

- Distribution of total minutes appear to follow a roughly normal distribution, centered around the mean. Majority of customers use a moderate number of total minutes, with fewer using extremely low or high total minutes.
- Distribution of total calls is also normal, suggesting a balanced call usage pattern. Most customers make an average number of calls, with fewer customers making an extremely low or high number of calls.
- Distribution of customer service calls shows a right-skewed histogram, indicating there are minimal spikes at higher values. This implies that customers rarely contact customer service. However, customers who call frequently (especially with 4 or more calls) might indicate service issues such as dissatisfaction, billing issues or technical problems which could correlate with churn.

- ### Relationship between churn and columns with numerical data
<img width="1072" height="856" alt="image" src="https://github.com/user-attachments/assets/75365ed2-9259-4b76-ae7f-72f4d1469f7e" />

- Number of Voicemail Messages vs churn
The majority of customers have a low number of voicemail messages.
There are many outliers at the upper end, suggesting some customers have significantly higher voicemail messages than the rest.
- Total Minutes vs churn
Non-churn customers: Total minutes appear to be centered around a slightly lower range.
Churned customers: These customers have a wider range of total minutes, with a higher median.
Customers with higher total usage might be more likely to churn, potentially due to high costs.
- Total Calls vs churn
Both churned and non-churned customers show similar distributions for total calls, with no major differences.
Total calls might not be a significant factor in predicting churn.
- Customer Service Calls vs churn
Non-churn customers: Fewer customer service calls, with most data concentrated at the lower range.
Churned customers: More customer service calls, with some extreme outliers.
High interaction with customer service is associated with churn, possibly indicating unresolved issues or dissatisfaction.

### Correlation Analysis
<img width="763" height="703" alt="image" src="https://github.com/user-attachments/assets/8381c421-710b-4cca-9acf-b8008c945bfa" />

- Strongly correlated variables (e.g., total day minutes and total day charge) might provide redundant information.
- Variables showing significant differences in correlations (positive or negative) with the target (churn) might be more predictive.
- Features with minimal correlation (close to 0) might have limited relevance to predictive modeling unless their relationship with the target (churn) is non-linear.

 Columns that are perfectly correlated provide redundant information, it's generally best to drop one of them to avoid multicollinearity and improve the model.
