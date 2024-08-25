# Zebedee Bank Loan Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [The Analysis](#the-analysis)
- [Results and Findings](#results-and-findings)
- [Recommendations](#recommendations)


## Project Overview
The goal is to build a Machine Learning Model to predict the loan to be approved or to be rejected for an applicant.
The Zebedee bank will decide whether to give a loan to the applicant based on some factors such as Applicant Income, Loan Amount, previous Credit History, Education, etc.

### Data Source

The Dataset was in CSV file format provided by [Kaggle](kaggle.com)

### Tools Used

- Excel - Data Cleaning [Download-here](https://microsoft.com)
- PowerBI - Analysis, and Creating the Report.

  ## The Analysis
### Data Cleaning and Preparation

Investigating the dataset to understand its structure, size, basic characteristics and understanding the type of data was the first thing I did.
Through MS Excel the cleaning processes I went through to prepare the data are as follows.
1.	Data Types: The “Dependents” column had a value “3+” which might be better represented as a numeric value.
2.	Inconsistent Data: There was an entry where “Gender” was blank, and “Dependents” were present. I simply used the “find and replace” option to transform it to N/A.
3.	Handled missing values in “Loan_Amount,” “Loan_Amount_Term,” and “Credit_History” columns which were denoted by blank cells.
4.	Addressed the inconsistency in the data, such as the entry with a blank “Gender.”

  ### Exploratory Data Analysis (EDA)

  I have generated the following key Performance Indicators (KPIs) and insights.
- Gender = 381
- Loan Amount given = 40M
- Self Employed = 36
- Average applicant income = 3.58K
- Credit history = 0.83%
- Loan Amount Average = 105.15K
- Loan Amount Approved = 29M (71.47%)
- Average Co-applicant income = 1.28K
- Loan amount by marital status = 25M (61.6%)
- Sum of applicant income by property area.
- Sum of applicant income by education
- Sum of applicant income by self employment
- Loan Amount by marital status
- Average loan amount by dependents

 ### Data Analysis

 Using Power BI, here are the formulas I used for my analysis (In the ‘Loan Approval Analysis by Zebedee Bank’).
- Gender = COUNTROWS (‘Loan Approval Analysis by Zebedee Bank’).
-	Loan Amount given = SUM (‘Loan Approval Analysis by Zebedee Bank’[Loan Amount]).
-	Self Employed = CALCULATE(COUNTROWS(‘Loan Approval Analysis by Zebedee Bank’), ‘Loan Approval Analysis by Zebedee Bank’[Self-employed]= “Yes”).
-	Average Applicant Amount = AVERAGE(‘Loan Approval Analysis by Zebedee Bank’[Applicant Income]).
-	%Credit History = DIVIDE(CALCULATE(COUNTROWS(‘Loan Approval Analysis by Zebedee Bank’, ‘Loan Approval Analysis by Zebedee Bank’[Credit History]=1, COUNTROWS(‘Loan Approval Analysis by Zebedee Bank’)).
-	Loan Amount Average = AVERAGE(‘Loan Approval Analysis by Zebedee Bank’[Loan Amount).
-	Average Co-applicant Income = AVERAGE (‘Loan Approval Analysis by Zebedee Bank’[Co-applicant income]).

   ## Design Considerations
  ### Data Visuals

1. Slicers: Were used to emphasize the key performance indicators.
2. Pie charts and Doughnut chart: Were used to show the relationship of parts to a whole in percentages.
3. Stacked column charts and Stacked bar charts: Were used to show the relationship between the applicants income and property area, education and self employment.
4. Line charts: Were used to show a relationship between loan term credit history by property area.

 ## Results and Findings

 Here are my findings for the Loan Approval Analysis by Zebedee Bank.
1.	A total of 381 customers got loans from the Zebedee Bank which is a good number.
2.	Majority of the customers are getting their loans approved (Yes) with 71.47%.
3.	Most of the customers getting loans are educated (Graduates).
4.	Semi urban area has the majority of people getting loans approved (Yes) with the least number of disapproved loans (No) followed by urban then rural areas.
5.	Most of the customers getting the loans from Zebedee Bank are employed as compared to the self employed customers.
6.	We can also see that unmarried customers are taking up more loans as compared to the married ones.
7.	Customers taking up loans prefer a longer period of payment as can be seen. The long term loan status (89.75%) has a higher percentage as compared to the short term status of (10.25%).
8.	Meanwhile in the average loan amount by dependents, at 110K, 3 had the highest Avg. Loan Amount higher than 0, which had the lowest Avg. Loan Amount at 103K. Across all the Dependents, Avg. Loan Amount ranged from 103 to 109.

  ## Recommendations
- Property Area and Income Insights: Explore business opportunities or tailor marketing strategies based on the regions with higher cumulative applicant income.
- Dependents and Loan Amounts: Assess whether the number of dependents is a crucial factor in determining the loan amount. This understanding can be used to refine loan product offerings.
- Try reviewing the loans policies so that most people (uneducated) are able to get approved loans.





