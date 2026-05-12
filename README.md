# Bank Marketing Campaign — EDA Analysis

## Project Overview
Performed end-to-end Exploratory Data Analysis (EDA) on a Bank Telemarketing Campaign dataset to identify key customer segments most likely to subscribe to a term deposit — helping the bank optimize its marketing strategy and improve campaign ROI.

---

## Business Problem
A bank conducts telemarketing campaigns to sell financial products like term deposits to customers. The challenge is — only ~11.7% of customers say YES. The bank needs to understand:
- Which customers are most likely to subscribe?
- What demographic and financial factors drive response?
- How can the bank target the right customers more efficiently?

---

## Dataset Description
- **Records:** 45,211 customers
- **Features:** 17 columns — demographic, financial and campaign data

| Column | Description |
|---|---|
| age | Customer age |
| job | Type of employment |
| education | Education level |
| marital | Marital status |
| salary | Annual salary |
| balance | Bank account balance |
| housing | Has housing loan? |
| loan | Has personal loan? |
| duration | Last call duration (seconds) |
| pdays | Days since last contacted |
| poutcome | Previous campaign outcome |
| response | **TARGET** — subscribed? Yes/No |

---

## Project Workflow

### 1. Data Cleaning
- Identified hidden missing values (-1 in pdays column)
- Handled missing values using median/mode imputation
- Removed duplicate records
- Standardized all string values to uppercase
- Created combined feature `jobedu` (job + education)

### 2. Outlier Treatment
- Detected outliers using IQR method (Q1 - 1.5×IQR to Q3 + 1.5×IQR)
- Applied capping technique — replaced extreme values with 99th percentile
- Treated outliers in balance, salary and duration columns

### 3. Univariate Analysis
- Analysed distribution of each variable individually
- Used histograms, boxplots and bar charts
- Found dataset is imbalanced — only 11.7% responded YES

### 4. Bivariate Analysis
- Numerical vs Numerical — scatter plots and correlation heatmap
- Numerical vs Categorical — boxplots comparing YES vs NO groups
- Categorical vs Categorical — response rate by each category

### 5. Multivariate Analysis
- Used get_dummies to convert categorical variables to binary
- Built correlation heatmaps across Education, Marital and Response
- Analysed combined effects of multiple variables on response rate

---

## Key Findings & Business Insights

| Finding | Insight |
|---|---|
| Single customers | 14.3% response rate — highest! |
| No personal loan | 13% response vs 7% with loan |
| No housing loan | Significantly higher response |
| Higher balance | Stronger predictor of YES |
| Tertiary education | Highest salary AND response rate |
| Age 18-25 and 60+ | Higher response than middle age |
| Longer call duration | Strong predictor of subscription |
| Previous success | Customers with past positive outcome respond more |

---

## Technologies Used
- **Python** — Core programming
- **Pandas** — Data manipulation and cleaning
- **NumPy** — Numerical computations
- **Matplotlib** — Base visualizations
- **Seaborn** — Statistical visualizations
- **SciPy** — Statistical analysis
- **Jupyter Notebook** — Development environment

---

## Skills Demonstrated
- Data Cleaning & Missing Value Treatment
- Outlier Detection using IQR Method
- Univariate, Bivariate and Multivariate Analysis
- Feature Engineering (jobedu combined feature)
- Statistical Analysis and Visualization
- Business Insight Generation from Data
