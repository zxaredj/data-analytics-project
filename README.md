# Employee Attrition Analysis Using Python

An end-to-end data analytics project investigating employee attrition patterns through data cleaning, exploratory data analysis, statistical hypothesis testing, and data visualization.

## Project Overview

Employee attrition is an important workforce management concern because employee departures can affect operational continuity, recruitment costs, and organizational performance.

This project analyzes employee demographic, educational, compensation-tier, location, and employment-related information to identify patterns associated with employee attrition.

Using Python, Pandas, NumPy, SciPy, Statsmodels, Matplotlib, and Seaborn, I performed data preparation, exploratory analysis, statistical testing, and business interpretation to transform raw employee records into actionable insights.

## Business Objectives

The project aims to:

- Calculate the overall employee attrition rate.
- Identify employee groups with higher observed attrition rates.
- Analyze attrition patterns across education, city, gender, payment tier, and bench status.
- Investigate numerical relationships involving age, joining year, and experience.
- Apply statistical tests to evaluate associations between employee characteristics and attrition.
- Develop data-driven recommendations to support workforce planning and retention strategies.

## Dataset Overview

The dataset contains 2,764 employee records and nine original attributes.

| Attribute | Description |
|---|---|
| Education | Employee educational qualification |
| JoiningYear | Year the employee joined |
| City | Employee location |
| PaymentTier | Employee payment classification |
| Age | Employee age |
| Gender | Employee gender |
| EverBenched | Whether the employee had previously been benched |
| ExperienceInCurrentDomain | Years of experience in the current domain |
| LeaveOrNot | Employee attrition indicator |

Target variable:

- `0` = Employee stayed
- `1` = Employee left

### Dataset Summary

| Metric | Result |
|---|---:|
| Total Employees | 2,764 |
| Employees Stayed | 1,676 |
| Employees Left | 1,088 |
| Overall Attrition Rate | 39.36% |

## Technologies and Libraries

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Excel

## Project Workflow

### 1. Data Loading and Inspection

- Loaded the employee dataset using Pandas.
- Inspected dataset dimensions, column names, and data types.
- Reviewed descriptive statistics and categorical distributions.
- Examined missing values and duplicate records.

### 2. Data Cleaning and Preprocessing

- Standardized column names and text values.
- Reviewed and handled missing values.
- Investigated duplicate records.
- Evaluated potential outliers using the Interquartile Range (IQR) method.
- Validated categorical values, numerical ranges, and business rules.
- Prepared the dataset for analysis.

### 3. Feature Engineering

Created additional analytical features to support employee attrition analysis, including attrition status and experience groupings.

### 4. Exploratory Data Analysis

Investigated employee attrition patterns across:

- Education
- City
- Gender
- Payment Tier
- Age
- Bench Status
- Experience in Current Domain
- Joining Year

Developed visualizations to compare attrition distributions and identify workforce patterns.

### 5. Statistical Hypothesis Testing

Applied the following statistical techniques:

**Chi-Square Test of Independence**

Used to investigate associations between categorical variables and employee attrition.

**Mann-Whitney U Test**

Used to compare numerical variable distributions between employees who stayed and employees who left.

**Point-Biserial Correlation**

Used to evaluate the direction and strength of relationships between numerical variables and the binary attrition outcome.

**Cramér's V**

Used to measure the strength of associations identified through categorical analysis.

**Benjamini-Hochberg Correction**

Applied to adjust p-values and control the false discovery rate across multiple statistical tests.

## Key Findings

### Overall Attrition

The dataset contains 1,088 employees who left out of 2,764 employees, representing an overall attrition rate of 39.36%.

### Attrition by Payment Tier

Payment Tier 2 recorded the highest observed attrition rate at 60.18%, compared with 35.32% for Tier 1 and 33.81% for Tier 3.

Payment tier also demonstrated the strongest categorical association with attrition among the variables tested (Cramér's V = 0.2173).

### Attrition by City

Pune recorded the highest observed attrition rate at 50.94%, followed by Bangalore at 35.01% and New Delhi at 34.09%.

### Attrition by Gender

Female employees recorded an observed attrition rate of 49.72%, compared with 31.00% among male employees.

### Attrition by Education

Employees with Master's degrees had the highest observed attrition rate at 48.51%, followed by Bachelor's degree holders at 37.49% and PhD holders at 25.64%.

### Attrition by Bench Status

Employees who had previously been benched recorded an attrition rate of 44.04%, compared with 38.66% among employees who had not been benched.

However, this relationship was not statistically significant at the 0.05 level after multiple-testing correction.

### Numerical Relationships

- Age had a weak negative correlation with attrition (r = -0.1149).
- Joining year had a weak positive correlation with attrition (r = 0.1506).
- Experience in the current domain had a negligible correlation with attrition (r = -0.0212).

## Statistical Analysis Summary

Six distinct variables demonstrated statistically significant associations with attrition after Benjamini-Hochberg correction:

- Payment Tier
- Gender
- Joining Year
- City
- Age
- Education

EverBenched and ExperienceInCurrentDomain did not meet the 0.05 significance threshold after correction.

## Business Recommendations

1. Review compensation structures and career progression opportunities, particularly for Payment Tier 2 employees.
2. Investigate location-specific workforce conditions in Pune.
3. Evaluate employee experience, career advancement opportunities, and workplace conditions across demographic groups.
4. Assess career development and role alignment for employees with advanced educational qualifications.
5. Monitor employee bench utilization and assignment duration.
6. Establish recurring workforce analytics reporting to monitor attrition patterns.

## Project Limitations

- The dataset does not contain actual salary amounts, so payment tier cannot be interpreted as a specific compensation value.
- Employee departure dates and observation-period information are unavailable.
- The analysis identifies statistical associations, not causal relationships.
- The findings are based on the available dataset and should not automatically be generalized to other organizations.
- The dataset does not include additional organizational factors such as department, manager, job satisfaction, or exit reasons.

## Repository Structure

```text
employee-attrition-analysis/
│
├── data/
├── notebooks/
├── reports/
├── visualizations/
├── README.md
├── requirements.txt
└── .gitignore
```

## Conclusion

This project demonstrates an end-to-end Python data analytics workflow, from raw data inspection and preprocessing to exploratory analysis, statistical hypothesis testing, and business recommendations.

It highlights how analytical techniques can be used to identify workforce patterns and translate statistical findings into meaningful business insights.

## Author

**Zxared Jay Mallillin**

AI Automation | Business Intelligence | Data Analytics

[LinkedIn](https://www.linkedin.com/)

[GitHub](https://github.com/)
