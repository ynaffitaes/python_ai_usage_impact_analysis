# AI Usage and Impact Analysis

## Overview

This project explores how students and professionals use Artificial Intelligence tools and how AI influences productivity, satisfaction, accuracy, and time savings.

Using survey data from 300 respondents, the project follows a complete data science workflow, including data cleaning, feature engineering, exploratory data analysis, statistical testing, and machine learning.

The goal is to understand the factors that drive AI adoption and user satisfaction while identifying the characteristics of users who benefit most from AI tools.

---

## Project Objectives

- Analyze AI adoption among students and professionals.
- Explore how AI usage affects productivity and time savings.
- Identify the most common AI tools and usage purposes.
- Investigate relationships between AI usage behavior and user outcomes.
- Predict user satisfaction using machine learning.
- Identify the key drivers of AI satisfaction.

---

## Dataset
Source: [Kaggle]([url](https://www.kaggle.com/datasets/eishatuzzuhra/ai-usage-and-impact-on-students-and-professionals/data))
The dataset contains information about:

- Demographics (Age, Gender, Country)
- Education and Profession
- Monthly Income
- Preferred AI Tool
- AI Usage Purpose
- AI Usage Hours
- Monthly AI Spending
- Productivity Score
- Accuracy Rating
- Satisfaction Score
- Time Saved Per Week
- Recommendation Behavior

### Size

- Records: 300
- Features: 19

---

## Data Cleaning

The following data quality issues were addressed:

- Standardized inconsistent categorical values
- Removed duplicate records
- Extracted numeric values from text-based columns
- Converted data types
- Handled missing values using domain-informed imputation
- Validated ranges and category consistency

Examples:

```text
"25 years" → 25
"$3,500" → 3500
"chatgpt" → "ChatGPT"
```

---

## Feature Engineering

Several additional features were created:

| Feature | Description |
|----------|------------|
| Weekly_AI_Usage_Hours | Daily usage × 7 |
| Productivity_Per_Hour | Productivity gained per hour of AI usage |
| Time_Saved_Per_AI_Hour | Weekly time saved per AI usage hour |
| AI_Cost_Efficiency | Weekly hours saved per dollar spent |
| High_AI_User | Users above median AI usage |
| Heavy_AI_Spender | Users above median AI spending |
| Productivity_Category | Low / Medium / High productivity |
| Satisfaction_Category | Low / Medium / High satisfaction |
| Income_Category | Low / Medium / High income |

---

## Exploratory Data Analysis

Key questions explored:

### User Comparison

- Do students use AI more than professionals?
- Are students more satisfied with AI tools?
- Which group gains more productivity from AI?

### AI Tool Analysis

- Which AI tools are most popular?
- Which tools generate the highest satisfaction?
- Which tools are associated with higher productivity?

### AI Purpose Analysis

- Why do people use AI?
- Which use cases provide the greatest time savings?
- Which activities benefit most from AI?
- Which AI purpose generates the highest productivity per hour of usage?

### Demographic Analysis

- AI adoption by country
- AI usage by age group
- AI usage by income level

### Engineered Feature Analysis

- Do heavy AI users achieve higher productivity?
- Do heavy AI users save more time?
- Does spending more money on AI increase efficiency?
- Which AI purposes generate the highest productivity per hour?

---

## Statistical Analysis

### Mann-Whitney U Test

**Question**

Do heavy AI users achieve higher productivity than regular users?

**Result**

The test revealed a statistically significant difference in productivity scores between heavy and regular AI users.

**Finding**

Users who engage more heavily with AI report significantly higher productivity levels.

---

### Chi-Square Test of Independence

**Question**

Is heavy AI spending associated with a specific AI usage purpose?

**Result**

No statistically significant relationship was found.

**Finding**

AI spending behavior appears relatively consistent across different AI purposes.

---

## Machine Learning

### Objective

Predict user satisfaction with AI tools.

### Target Variable

```text
Satisfaction_Score
```

### Models

- Linear Regression
- Random Forest Regressor

### Results

| Model | MAE | RMSE | R² |
|---------|---------|---------|---------|
| Linear Regression | 0.891 | 1.12 | 0.475 |
| Random Forest | 0.916 | 1.07 | 0.52 |

### Best Model

Random Forest Regressor

The model explained approximately 52% of the variation in user satisfaction.

---

## Key Findings

- Productivity is the strongest predictor of AI satisfaction.
- Accuracy is the second most important factor influencing satisfaction.
- Users value the outcomes achieved with AI more than simple usage volume.
- Heavy AI users report substantially higher productivity.
- Higher spending does not necessarily lead to greater efficiency.
- Time savings play an important role in improving satisfaction.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn

---

## Business Conclusion

The analysis suggests that user satisfaction is primarily driven by the practical value users obtain from AI rather than by demographic characteristics or spending levels. Productivity improvements, output accuracy, and time savings are the strongest factors associated with positive AI experiences.

## Author

Aram Samb
