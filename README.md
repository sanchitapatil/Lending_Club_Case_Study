# Risk Analytics in Consumer Lending
> Using Exploratory Data Analysis (EDA) to Minimize Credit Loss

## Table of Contents
* [General Information](#general-information)
* [Business Understanding](#business-understanding)
* [Data Understanding](#data-understanding)
* [Analysis Approach](#analysis-approach)
* [Reusable Functions for Visualizations](#reusable-functions-for-visualizations)
* [Findings and Conclusions](#findings-and-conclusions)
* [Technologies Used](#technologies-used)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)


## General Information
This project aims to analyze risk factors in consumer lending to minimize financial losses for a finance company. The company needs to effectively assess loan applications to avoid two primary risks: losing business by rejecting good applicants and incurring financial losses by approving bad applicants. The objective is to identify patterns indicating loan default to inform better decision-making.

## Business Understanding
The project is conducted for the largest online loan marketplace, which facilitates personal, business, and medical loans. The critical risk involves lending to risky applicants, leading to significant financial losses. The goal is to understand the drivers of loan default and reduce credit loss.

## Data Understanding
The dataset contains information on past loan applicants from 2007 to 2011. The analysis focuses on identifying variables that indicate a higher risk of loan default. Key variables include:

- **Employment-related**: Employment_Title, Employment_Length
- **Financial**: Annual_Income, Debt_to_Income_Ratio
- **Credit History**: Number_of_Delinquencies_in_the_Last_2_Years, Earliest_Credit_Line_Month, Number_of_Inquiries_in_the_Last_6_Months, Number_of_Open_Credit_Accounts, Number_of_Public_Records, Number_of_Public_Record_Bankruptcies
- **Loan-related**: Loan_Amount, Loan_Term, Interest_Rate, Monthly_Installment, Credit_Grade, Credit_Subgrade, Income_Verification_Status, Loan_Purpose, Loan_Title, Revolving_Balance, Revolving_Utilization_Rate, Total_Number_of_Credit_Accounts, Home_Ownership_Status
- **Loan Status**: Loan_Status (Fully Paid, Charged-off)

## Analysis Approach
The analysis approach involves several steps:

1. **Data Loading**
2. **Data Exploration**
3. **Data Cleaning**
   - Identifying and removing redundant columns
   - Dealing with missing values
   - Treating outliers and transforming data for analysis readiness
4. **Exploratory Data Analysis (EDA)**
   - Univariate Analysis
   - Segmented Univariate Analysis
   - Derived Metrics
   - Bivariate Analysis

## Reusable Functions for Visualizations
To streamline the data analysis process, custom reusable functions were created for various visualizations used in univariate, segmented univariate, and bivariate analysis.

### Pros of Reusable Functions:
1. **Consistency**: Ensures that all visualizations follow the same style and format, making it easier to compare and interpret results.
2. **Efficiency**: Saves time and effort by avoiding repetitive code. Once a function is written, it can be used multiple times across the project.
3. **Scalability**: Allows for easy updates and modifications. If a change is needed, it can be made in the function, and all visualizations will be updated accordingly.
4. **Readability**: Improves code readability and organization. Functions encapsulate specific tasks, making the main analysis script cleaner and easier to understand.

## Findings and Conclusions
Key findings from the analysis include:

- **Credit Grade**: Grades B, C, D, E, F, G have high default rates
- **Debt-to-Income Ratio (DTI)**: DTI > 13 indicates potential financial strain.
- **Home Ownership Status**:  Renters or Mortgage holders provide stable housing situations.
- **Number of Delinquencies**: Any delinquencies suggest past payment issues.( >0).
- **Credit Utilization Ratio**: High ratios (> 0.6) indicate potential financial stress.
- **Interest Rate**:Rates between 13.23% and 14.11% associated with higher defaults.
- **Number of Inquiries per Account**: High inquiries (> 0.09) may signal financial distress.
- **Loan Purpose**: High-risk purposes like debt_consolidation, credit_card, small_business, other are correlated with higher default rates.
- **Employment Length**: Short (< 2 years) or long (>= 10 years) lengths suggest instability.
- **Number of Open Credit Accounts**: More the median indicates higher credit exposure. ( >8)

Recommendations based on the analysis:

- Implement stricter approval criteria for higher loan amounts and high-risk loan purposes.
- Monitor borrowers with higher DTI ratios and past delinquencies more closely.
- Strengthen income verification processes.
- Exercise caution when lending to renters and borrowers with lower credit grades.

## Technologies Used
- Python 3.11.7 
- Pandas 2.1.4
- Seaborn 0.12.2
- Matplotlib 3.8.0

## Acknowledgements
This project was inspired by real-world challenges faced in consumer lending and is based on various references and tutorials on risk analytics and EDA techniques.

## Contact
Created by [@sanchitapatil](https://sanchitapatil.github.io/) - feel free to contact me!
