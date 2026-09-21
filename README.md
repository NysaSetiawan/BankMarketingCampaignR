# Bank Marketing Campaign Analysis

## 📌 Overview

An end-to-end data analysis project exploring customer characteristics and marketing campaign interactions to understand factors associated with term-deposit subscription.

Using R and interactive visualization techniques, this project covers the complete analytical workflow from data quality assessment and preprocessing to exploratory analysis, feature engineering, relationship analysis, data storytelling, and business recommendations.

The project was developed as part of the **Data Mining and Visualization** course at BINUS University.

---

## 🎯 Objectives

The project aims to:

- Assess and improve the quality of bank marketing campaign data
- Identify customer and campaign characteristics associated with subscription outcomes
- Engineer new features to enhance customer segmentation and behavioral analysis
- Explore relationships between customer attributes and campaign performance
- Develop interactive visualizations to communicate analytical findings
- Translate findings into actionable business recommendations

---

## 🛠️ Tools & Technologies

- **R**
- **R Markdown**
- **dplyr**
- **ggplot2**
- **Plotly**
- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Feature Engineering
- Interactive Data Visualization
- Data Storytelling

---

## 🔍 Analysis Workflow

### 1. Data Quality Assessment

The dataset was examined for several data quality issues, including:

- Missing values
- Duplicate records
- Inconsistent categories
- Outliers
- Noisy values

The analysis identified missing values in the `duration` variable, inconsistent `"unknown"` and empty values across several categorical variables, and the special `999` value in `pdays`.

### 2. Data Preprocessing

Several preprocessing techniques were applied:

- Converted the `pdays` variable into meaningful recency categories
- Replaced `"unknown"` and empty values with `NA`
- Imputed missing categorical values using the **mode**
- Imputed missing numerical values using the **median**
- Applied **IQR-based winsorization** to cap extreme values
- Created a cleaned dataset named `clean_data`

The `pdays = 999` value was retained and transformed rather than removed because it represents customers who had not previously been contacted.

---

### 3. Exploratory Data Analysis

Statistical summaries were generated to examine:

- Mean
- Median
- Mode
- Standard deviation
- Variance
- IQR
- Minimum and maximum values
- Range

Additional grouped summaries were used to examine customer age across multiple demographic and campaign-related categories.

---

### 4. Customer & Campaign Relationship Analysis

The relationship between customer characteristics and campaign outcomes was explored using cross-tabulation and conversion rates.

Several dimensions were analyzed, including:

- Job
- Marital status
- Education level

For example, the analysis found that **students and retired clients showed relatively high conversion rates**, at approximately **24.59% and 29.35%**, respectively.

Marital status analysis showed that **single clients had a higher conversion rate of approximately 13.17%** compared with other marital-status groups.

Education-level analysis found that **university graduates had a 13.23% conversion rate**, while high-school graduates had a **12.06% conversion rate**.

---

### 5. Feature Engineering

Three new features were created to improve customer-level analysis:

| Feature | Description |
|---|---|
| `age_group` | Segments customers into `<30`, `30–50`, and `>50` |
| `recency_level` | Categorizes previous contact into `never`, `recent`, and `old` |
| `total_contact_score` | Combines current and previous campaign contacts |

These features were designed to provide additional perspectives on customer demographics, campaign recency, and engagement.

---

### 6. Interactive Data Visualization

Interactive visualizations were developed using **Plotly** to investigate different types of relationships.

#### Education vs. Marital Status

A grouped bar chart was used to compare education levels across marital-status categories.

The analysis showed that married customers represented the largest group, while university-degree holders were the most numerous education category across marital statuses.

#### Age Distribution Across Job Levels

A boxplot was created to examine age distributions across job categories.

Key observations included:

- Retired customers had the highest median age at approximately **59**
- Students represented the youngest group with a median age of approximately **26**
- Several job categories showed noticeable age variation and outliers

#### Age, Contact Method & Housing Loan

A multidimensional histogram was created using age, contact method, and housing-loan status.

The visualization showed that **cellular communication was the dominant contact method**, with particularly high activity among customers aged approximately 30–40.

---

## 📊 Data Storytelling

Two focused visual stories were developed to communicate business-relevant findings.

### Loan Types by Marital Status

Among customers who subscribed to a term deposit:

- Married customers had a **53% housing-loan rate**
- Married customers had a **17.1% personal-loan rate**
- Single customers had a **52.6% housing-loan rate**
- Divorced customers showed the lowest personal-loan rate at **11.8%**

The analysis also acknowledges that these relationships represent associations rather than causal effects.

### Term Deposit Subscription by Education

The analysis showed that:

- University graduates achieved a **13.23% conversion rate**
- High-school graduates achieved a **12.06% conversion rate**
- Basic education groups generally showed lower conversion rates
- The illiterate group showed the highest observed conversion rate at approximately **16.6%**, but represented a very small portion of the dataset, making this result potentially unreliable

---

## 💡 Business Recommendations

Based on the analysis, two recommendations were developed:

1. **Target married customers with bundled financial offers** involving housing and personal loans, given their relatively high engagement with both loan categories.

2. **Prioritize university-degree and high-school customers in future campaigns**, as these groups combine substantial representation in the dataset with relatively strong subscription conversion rates.

---

## 📈 Key Skills Demonstrated

This project demonstrates practical experience in:

- Data Cleaning & Preprocessing
- Missing Value Imputation
- Outlier Detection & Winsorization
- Exploratory Data Analysis
- Statistical Summarization
- Customer Segmentation
- Feature Engineering
- Cross-tabulation & Conversion Rate Analysis
- Interactive Data Visualization
- Plotly
- Data Storytelling
- Business Insight Generation
- Data-driven Recommendations
