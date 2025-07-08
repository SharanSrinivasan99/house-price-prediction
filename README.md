# 🏠 House Price Prediction 
This project focuses on predicting house prices using regression models. It aims to identify the features that influence price the most and evaluate which model performs best for this type of structured data.

## 💼 Business Context

Real estate pricing can be volatile and influenced by multiple, often messy, variables. The aim is to:
- Predict the **sale price** of a house accurately.
- Understand what **factors** matter most when pricing a property.
- Provide insights that reduce **financial risk** for buyers, sellers, and agents.

## 📊 Dataset Overview

- 2,908 observations  
- 81 features: 43 categorical, 38 numerical  
- Common issues: **missing values**, **outliers**, **feature sparsity**

We cleaned the data using:
- Domain-based imputation (`No Garage`, `Not Applicable`, etc.)
- Feature transformation (e.g., grouping quality ratings)

## 🔍 Feature Selection Strategies

Two modelling approaches were explored:
1. **Statistical filtering** – drop insignificant features.
2. **All-in approach** – use every feature and let regularisation handle it.

## ⚙️ Models Compared

- **Linear Regression**
- **Ridge Regression** 🔥 (Winner!)
- **Lasso Regression**

### Model Performance (Unseen Data)

| Model              | Approach 1 | Approach 2 |
|-------------------|------------|------------|
| Linear Regression | $25,893    | $18,600    |
| Ridge Regression  | $18,600    | $18,600    |
| Lasso Regression  | $45,444    | $33,479    |

## 🔑 Key Features Identified

Some of the features with the most influence:
- Overall condition and quality
- Basement area
- Home functionality rating

## ⚠️ Notes and Limitations

- The data is region-specific and may not generalise well
- Some macroeconomic variables (like interest rates) weren’t included
- Regularisation helps avoid overfitting, but results may vary across datasets

## 💬 Final Takeaway

📉 Ridge Regression emerged as the most robust model, balancing complexity with predictive accuracy. The model shines when all features are included — because, apparently, more **is** more (with the right regularisation, of course).

> “Good data prep goes a long way. The models just help bring it home.”
---
---
