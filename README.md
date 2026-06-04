# Student Loan Debt Analysis

## Overview
Statistical analysis exploring the relationship between college rankings, 
tuition, and student loan burden across U.S. institutions. Merges federal 
student loan disbursement data with college rankings to model average loan 
burden per student.

## Data
Two datasets merged on school name (not included in repo — loaded locally):
- `Student_Loan_Debt.csv` — federal loan origination and disbursement data 
  by school and loan type
- `College_Rankings.csv` — college rankings, tuition, and enrollment numbers

## Methods
- Data cleaning, merging, and aggregation by school using dplyr
- Correlation analysis (rank vs. loan burden, tuition vs. loan burden)
- Simple and multiple linear regression with diagnostic plots 
  (residuals, Q-Q, Cook's distance)
- Monte Carlo simulation (10,000 iterations) modeling loan amounts 
  across random tuition values
- One-sample t-test comparing mean loan to a $25,000 baseline
- 95% confidence intervals for mean loan amount
- Loan efficiency analysis (originated vs. disbursed amounts)
- Boxplot visualization by rank group using ggplot2

## Key Findings
- Tuition is a significant predictor of loan burden (r = 0.37, p < 0.001)
- School rank alone is not a significant predictor (r = -0.09, p = 0.376)
- Combined rank + tuition model explains 16.6% of variation in avg loan
- 95% CI for true mean loan: [$229,144 — $304,738]
- Monte Carlo simulation revealed tuition alone vastly underpredicts 
  real-world loan amounts, suggesting other factors (financial aid, 
  cost of living, income) play a major role

## Tools & Libraries
R, RMarkdown, tidyverse, dplyr, ggplot2, base R stats
