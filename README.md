# Credit-Risk-Analysis-PowerBI-Python
A Power BI + Python dashboard for credit default analysis, clustering, and logistic regression using customer financial data.

This project presents an end-to-end credit risk analysis using Power BI and Python. The dashboard blends exploratory data analysis (EDA), machine learning (logistic regression and clustering), PCA, and visual storytelling to understand and predict customer payment default behavior.

---

## Project Overview

The dataset contains demographic and financial records of 30,000 credit card customers. Fields include gender, education, marital status, age, credit limit, bill amounts, repayment status, and payment default status.

The Power BI dashboard includes:
- Visual segmentation by gender, education, and age groups
- Default rate analysis
- Outlier detection using Python visuals
- Logistic regression modeling
- PCA transformation for dimensionality reduction
- K-means clustering for customer segmentation
- Key Influencers and Decomposition Tree analysis

Python visuals were embedded directly into Power BI for predictive modeling, PCA, and clustering.

---

## Key Assumptions & Data Transformations

- **Data Cleaning**:
  - Removed 3 empty columns
  - Promoted the first row to headers
  - Confirmed no missing values remained in the dataset

- **Renaming for Clarity**:
  - `LIMIT_BAL` → `Credit Limit`
  - `SEX` → `Gender`
  - `EDUCATION` → `Education`
  - `MARRIAGE` → `Marriage Status`
  - `default.payment.next.month` → `Default payment next month`
  - Renamed `PAY`, `BILL`, and `AMT` fields with readable labels (e.g., `Repayment Status 0`, `Bill Amount 1`)

- **Value Mapping (based on UCI Reference Dataset)**:
  - **Education**:
    - 0 = Unknown
    - 1 = Graduate (Master’s, PhD)
    - 2 = University (Bachelor’s)
    - 3 = High School
    - 4/5/6 = Others
  - **Marriage Status**:
    - 0 = Unknown
    - 1 = Married
    - 2 = Single
    - 3 = Others
  - **Gender**:
    - 1 = Male
    - 2 = Female

These assumptions ensured data consistency and alignment with the [UCI Machine Learning Repository dataset](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients), while accommodating the actual values observed in our version of the dataset.

---

## Dashboard Views

### 1. Exploratory Data Analysis (EDA)
- Gender, age group, education distribution
- Default vs non-default comparison
- Outlier detection using scatter/box plots

### 2. Credit Limit Analysis
- Decomposition Tree exploring patterns across gender, age, and education
- Identifies groups with the highest average credit limit

### 3. Key Drivers of Default
- Key Influencers chart showing top factors affecting likelihood of default
- Repayment status emerged as the strongest predictor

### 4. Machine Learning & AI Insights
- **Logistic Regression** model using Average Bill, Credit Limit, and Repayment Status  
  - Accuracy: 79.64% | Precision: 66.74% | Recall: 16.34% | F1 Score: 26.25%
- **Customer Clustering** (k=4) to segment customer profiles
- **Principal Component Analysis (PCA)**: 2D visual showing customer distribution by behavior

---

## Tools & Techniques

- **Power BI Desktop**
- **Python Libraries:** `pandas`, `matplotlib`, `scikit-learn`, `seaborn`, `kneed`
- **DAX Measures**: Total Customers, Average Bill, Repayment Status, Grouped Labels
- **AI Visuals**: Key Influencers, Clustering, PCA, Logistic Regression
- **Interactive Filtering**: Slicers for education, age group, gender, repayment status

---

## Contribution

This was a team project.

- **I developed all Python visuals and scripts**, implemented **DAX measures**, and selected the **final visual design and analytics techniques** used throughout the report.  
- **Lhagii** contributed to the design and dashboard visuals, making the interface more visually pleasing.  
- **Mihir** provided feedback and suggestions to improve the Python visuals and the clarity of the box plot.

---

## Files Included

- `CreditRiskDashboard.pbix` – Main Power BI file with embedded Python code
- `Images/` – Preview screenshots of major dashboards and ML results
- `credit card clients.xlsx` - This is the dataset that we used for our dashboard. This is similar to the dataset from the **Reference** but not the same. 

---

## Reference

Dataset source:  
[UCI Machine Learning Repository – Default of Credit Card Clients](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)

---

## Author

Tha Pyay Hmu  
