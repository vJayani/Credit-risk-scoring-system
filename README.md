# Credit Risk Scoring System

## Project Overview

This project implements an end-to-end **Credit Risk Scoring System** that predicts the likelihood of a loan applicant defaulting.  
The solution uses historical applicant information and machine learning to support **data-driven, fair, and explainable credit decisions**.

The project is designed to reflect a real-world banking use case while being implemented within a **hackathon time constraint**.

## Hackathon Context

This solution was developed during a **4-hour hackathon**.  
Given the limited time, the focus was on building a **clean, explainable, and production-style pipeline** using the most informative dataset, while keeping the design extensible for future data sources.

## Business Objective

Financial institutions must balance growth and risk when approving loans.  
Traditional rule-based systems are rigid and may fail to capture complex risk patterns.

**Objectives of this project:**
- Predict the probability of loan default
- Reduce financial losses from high-risk approvals
- Improve approval rates for low-risk customers
- Provide transparent and explainable risk scores
- Enable fairness monitoring across demographic groups

## Use Case

Build a data-driven credit risk model that estimates the probability of default using:
- Financial information
- Behavioral indicators
- Credit-related historical signals

## Dataset

### Primary Dataset
- **Home Credit Default Risk – `application_train.csv`**

This dataset includes:
- Applicant demographics
- Employment and income details
- Loan amount and repayment information
- Credit-related historical indicators
- Target variable:
  - `0` → Non-default
  - `1` → Default

> Note:  
> The application dataset already contains **aggregated financial, behavioral, and bureau-derived features**.  
> Due to hackathon time constraints, raw bureau and transaction-level datasets were not merged, but the pipeline is designed to support them in future iterations.

## Data Access

Due to GitHub file size limitations, the dataset is not included in this repository.

You can download the dataset from Kaggle:
- Home Credit Default Risk: https://www.kaggle.com/c/home-credit-default-risk/data

After downloading, place `application_train.csv` inside the `data/` folder.
## End-to-End Workflow

Data Ingestion
↓
Data Cleaning & Validation
↓
Feature Engineering
↓
Feature Encoding
↓
Model Training
↓
Evaluation
↓
Insights & Visualization

## Data Processing

### Data Quality Checks
- Missing value analysis
- Data type validation
- Duplicate record handling
- Basic outlier inspection

### Data Cleaning & Transformation
- Imputation of missing values
- Standardization of numeric features
- Consistent formatting of categorical values

### Feature Engineering
- Income and loan-related financial features
- Employment and demographic indicators
- Credit behavior signals derived from historical attributes

### Feature Encoding
- One-hot encoding for categorical variables
- Numerical feature preparation for modeling

## Machine Learning Model

- **Algorithm:** LightGBM (Gradient Boosting)
- **Reason for selection:**
  - Strong performance on tabular data
  - Fast training time
  - Widely used in credit risk modeling

### Train–Validation Strategy
- 80% training data
- 20% validation data

## Model Evaluation

**Evaluation Metrics**
- AUC-ROC
- KS Statistic

### Results Summary
- AUC-ROC: ~0.80+
- KS Statistic: ~30+
- The model demonstrates good separation between defaulters and non-defaulters

## Explainability & Fairness

- Feature importance analysis used to understand key risk drivers
- Fairness check performed by comparing average risk scores across gender
- Designed to align with responsible AI and regulatory expectations

## Visualization (Conceptual)

- Distribution of predicted risk scores
- Model performance metrics (AUC, KS)
- Feature importance insights
- Fairness comparison across demographic groups

## Repository Structure

credit-risk-scoring-system
├── Credit Risk Scoring System.ipynb
├── README.md
└── data
    └── .gitkeep

## How to Run

1. Clone the repository  
2. Download `application_train.csv` from Kaggle  
3. Open the Jupyter Notebook  
4. Run all cells sequentially  

## Future Enhancements

- Integrate raw credit bureau data for deeper credit history analysis
- Add transaction-level behavioral features
- Deploy the model as an API for real-time scoring
- Implement automated monitoring dashboards
- Apply advanced bias mitigation techniques

## Key Takeaway

This project demonstrates how a **practical, explainable, and business-ready credit risk model** can be built efficiently under time constraints, while remaining aligned with real-world banking requirements.


