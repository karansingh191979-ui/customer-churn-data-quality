# Customer Churn Dataset — Data Quality Summary

## Purpose
Create a reproducible, analysis-ready version of the supplied synthetic customer churn dataset and document the data-quality checks performed.

## Dataset overview
- Original records: 15
- Columns: 11
- Rows retained after cleaning: 15
- Dataset scope: small synthetic customer sample; conclusions are descriptive and should not be generalized to a real customer population.

## Findings
- Missing cells before cleaning: 0
- Exact duplicate rows before cleaning: 0
- Missing cells after cleaning: 0
- Exact duplicate rows after cleaning: 0
- Churned customers (`Churn = Yes`): 7 of 15 (46.7%)
- Average age: 39.07 years
- Average tenure: 18.80 months
- Average monthly charges: 84.66
- Median total charges: 1099.78

## Cleaning steps and assumptions
1. Loaded the original CSV and preserved a separate original copy in the analysis workbook.
2. Trimmed leading/trailing whitespace in text columns.
3. Converted expected numeric fields (`Age`, `TenureMonths`, `MonthlyCharges`, `TotalCharges`, `SupportTickets`) to numeric types. Invalid values would become missing and be reviewed; none were introduced in this sample.
4. Checked missing values and exact duplicate rows. No rows were removed because no exact duplicate rows were found.
5. Scanned numeric fields for potential outliers using the 1.5 × IQR rule. Potential outliers are flags for review, not automatic errors; no values were removed solely because of this statistical rule.
6. Preserved all 15 records and all 11 columns.

## Validation checks
- Row count preserved: True
- Column count preserved: True
- No missing cells after cleaning: True
- No exact duplicate rows after cleaning: True
- `CustomerID` unique: True
- Age values between 0 and 120: True
- Tenure values non-negative: True
- Monthly and total charges non-negative: True
- Support tickets non-negative: True
- Churn labels limited to Yes/No: True

## Interpretation
This sample is already structurally tidy: it contains no missing cells or exact duplicate rows, and the expected numeric columns are numeric. The cleaning work therefore focuses on consistent text trimming, explicit type handling, profiling, and validation rather than deleting data. The churn rate in this 15-row synthetic sample is 46.7%; it is too small and synthetic to support business-wide conclusions.

## Reproducibility
The accompanying Excel workbook includes the original data, cleaned data, column profile, numeric summary statistics, categorical distributions, IQR outlier scan, validation checks, and cleaning assumptions. The cleaned CSV is the analysis-ready export.
