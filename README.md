# Veteran Status and Earnings: Evidence from IPUMS Data

## Overview
This project examines the effect of veteran status on wage income using IPUMS USA data. The analysis uses OLS regression with progressively richer controls to evaluate how the estimated effect changes across specifications.

## Research Question
What is the effect of veteran status on log wage income?

## Data
Data comes from IPUMS USA (American Community Survey, 2010–2019).

## How to Obtain Data
1. Go to https://usa.ipums.org/usa/
2. Create an account
3. Select ACS data for 2010–2019
4. Extract the following variables:
   - SEX
   - VETSTAT
   - INCWAGE
   - EDUCD
   - OCC2010
   - DEGFIELD
   - VETDISAB
   - DIFFCARE
   - DIFFREM
   - METRO
   - AGE
5. Download as a CSV file and place it in your project folder. 

## Data Processing
- Restrict to individuals with INCWAGE > 0
- Construct log wage:
  log_wage = log(INCWAGE)
- Create indicators for:
  - Veteran status
  - Gender

## Methodology
The analysis estimates the following models:
1. Raw regression: log(wage) on veteran status
2. Controls: adds age and gender
3. Fixed effects: adds year effects
4. Full model: adds occupation and degree field fixed effects

## How to Run
Open `Gitrmd.rmd` in RStudio and click “Knit” to reproduce all results, or run the code chunks sequentially.

## Key Finding
The estimated effect of veteran status on wages is highly sensitive to model specification. While the raw regression suggests a wage premium, controlling for observable characteristics reverses the sign, indicating that composition effects drive the initial result.

## Data Availability
Raw IPUMS data are not included in this repository due to data use restrictions. Users must download the data directly from IPUMS.

## Author
Aiden Black  

Undergraduate Student, University of Florida

Email: aiden.black@ufl.edu
