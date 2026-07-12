# Diabetes-Risk-Statistical-Analysis
Statistical analysis of diabetes risk factors using Excel — descriptive statistics, hypothesis testing, and correlation analysis on the Pima Indians dataset
# Diabetes Risk Statistical Analysis

A statistical analysis of health metrics associated with diabetes risk, built in Excel using the Pima Indians Diabetes dataset. The project applies descriptive statistics, hypothesis testing, and correlation analysis to identify which health indicators are most strongly linked to diabetes outcomes.

## 📊 Overview

This project analyzes 768 patient records to answer a core question: **which health metrics best predict diabetes risk?** The analysis moves from raw data cleaning through to statistical testing and visualization, following a complete end-to-end analytics workflow.

**Dataset:** Pima Indians Diabetes Dataset
**Records:** 768 patients
**Variables:** Pregnancies, Glucose, Blood Pressure, BMI, Diabetes Pedigree Function, Age, Outcome (0 = Non-Diabetic, 1 = Diabetic)

## 🛠️ Tools Used

- **Microsoft Excel** (Advanced)
- **Power Query** — data cleaning and transformation
- **Data Analysis ToolPak** — hypothesis testing (t-test)
- **Pivot Tables** — cross-verification of statistics
- **Excel Charts** — data visualization

## 🔧 Methodology

### 1. Data Cleaning
- Applied median imputation for missing/invalid values using Power Query
- Removed columns with high missingness that would skew analysis
- Validated data types and ranges for all variables

### 2. Descriptive Statistics
Calculated Mean, Median, and Standard Deviation for key variables (Glucose, Blood Pressure, BMI, Age), segmented by diabetes outcome, using:
- `AVERAGEIF()` for means
- `MEDIAN(IF())` array formulas for medians
- `STDEV.S(IF())` array formulas for standard deviations

### 3. Pivot Table Verification
Cross-checked all descriptive statistics against pivot table outputs to confirm formula accuracy — a critical QA step before drawing conclusions.

### 4. Hypothesis Testing
Ran a **two-sample t-test (assuming unequal variances)** to test whether Glucose levels differ significantly between diabetic and non-diabetic groups.

### 5. Correlation Analysis
Used `CORREL()` to measure the strength of relationship between each health metric and diabetes outcome.

## 📈 Key Findings

| Metric | Non-Diabetic (Avg) | Diabetic (Avg) | Correlation with Outcome |
|---|---|---|---|
| **Glucose** | 110.7 | 142.1 | **0.49** (strongest) |
| **BMI** | 30.9 | 35.4 | 0.31 |
| **Age** | 31.2 | 37.1 | 0.24 |
| **Pregnancies** | — | — | 0.22 |
| **Diabetes Pedigree Function** | — | — | 0.17 |
| **Blood Pressure** | 70.9 | 75.1 | 0.17 (weakest) |

- **Glucose is the strongest predictor of diabetes** in this dataset (r = 0.49). The difference in average glucose between diabetic and non-diabetic patients is statistically significant (t-test, p < 0.001).
- **BMI is the second-strongest indicator** (r = 0.31), with diabetic patients averaging a notably higher BMI.
- **Blood Pressure showed the weakest relationship** with diabetes outcome, suggesting it is a less reliable standalone predictor.

**Conclusion:** Glucose level and BMI are the most reliable indicators for identifying diabetes risk in this population and could serve as priority screening metrics.

## 📊 Charts

**Correlation of Health Metrics with Diabetes Outcome**
*(add screenshot: `images/correlation_chart.png`)*

**Average Health Metrics: Diabetic vs Non-Diabetic**
*(add screenshot: `images/group_comparison_chart.png`)*

## 📁 Repository Structure

```
├── diabetes_PROJECT_STATE.xlsx # Full workbook (raw data, cleaning, analysis, charts)
├── images/ # Chart screenshots
└── README.md
```

## 🚀 How to Use

1. Download `diabetes_PROJECT_STATE.xlsx`
2. Open in Microsoft Excel (2016 or later recommended for full formula compatibility)
3. Explore tabs in order: `diabetes` (raw) → `CLEAN DATA` → `DESCRIPTIVE STATISTIC` → `P-VALUE AND CORRELATION` → `PIVOT TABLE`

## 👩‍💻 About

Built as part of a Data Analytics portfolio during my transition from Life Sciences to Data Analytics. Connect with me on [LinkedIn](https://www.linkedin.com/in/jyoti-169486366).

---
*Part of an ongoing data analytics portfolio — see also: [Swiggy Restaurant Analysis](https://github.com/jyoti-analytics1405/Swiggy-Restaurant-Analysis)*
