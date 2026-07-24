# Telecom Retention Campaign Analysis using Causal Inference

## Overview

This project investigates the true impact of customer retention offers on telecom customer churn using causal inference techniques.

Unlike traditional machine learning models that predict churn, this project estimates whether retention campaigns actually reduce churn after accounting for selection bias and confounding variables.

The analysis combines multiple causal inference methods with customer segmentation to identify which customer groups benefit the most from retention offers and evaluates the financial impact of targeted interventions.

---

## Problem Statement

Telecom companies invest heavily in retention campaigns to reduce customer churn. However, customers receiving offers are typically high-risk customers rather than randomly selected individuals.

As a result, directly comparing churn rates between treated and untreated customers leads to biased conclusions.

This project addresses this problem by estimating the causal effect of retention offers using modern causal inference techniques.

---

## Objectives

- Explore telecom customer and campaign data
- Estimate the overall causal effect of retention offers
- Compare multiple causal inference estimators
- Identify customer segments using K-Means clustering
- Estimate heterogeneous treatment effects across segments
- Evaluate the financial impact and ROI of targeted retention campaigns
- Generate business recommendations

---

## Dataset

Modified IBM Telco Customer Churn Dataset

Target Variables:

- **Treatment:** `Received_Offer`
- **Outcome:** `Churn_Final_Flag`

The dataset also includes simulated business variables such as:

- Customer Value
- Offer Cost
- Expected Revenue Saved
- Expected Net Value
- True Treatment Effect

---

## Methodology

### 1. Exploratory Data Analysis

- Customer churn distribution
- Treatment distribution
- Treatment vs churn
- Contract distribution
- Relationship between tenure and monthly charges
- Business summary statistics

---

### 2. Overall Causal Analysis

The following causal inference techniques were implemented:

- Naïve Difference
- Propensity Score Estimation
- Propensity Score Matching (PSM)
- Inverse Probability Weighting (IPW)
- Doubly Robust Estimation
- DoWhy Structural Causal Model

Robustness was further evaluated using:

- Random Common Cause Refuter
- Placebo Treatment Refuter
- Data Subset Refuter

---

### 3. Customer Segmentation

Customer segments were identified using:

- Random Forest feature importance
- Confounder ranking
- Feature selection
- K-Means clustering
- Cluster evaluation
- Customer profiling

---

### 4. Heterogeneous Treatment Effects

Causal effects were estimated separately for each customer segment to identify groups that benefit most from retention campaigns.

---

### 5. Financial Impact Analysis

Business metrics evaluated include:

- Offer Rate
- Revenue Saved
- Estimated Churn Reduction
- Net Value
- Return on Investment (ROI)

---

## Key Results

- Naïve estimates substantially overestimated campaign effectiveness due to selection bias.
- Propensity-based methods consistently estimated a negative treatment effect, indicating that retention offers reduce customer churn.
- Customer segmentation revealed heterogeneous treatment effects across different customer groups.
- Premium at-risk customers demonstrated the highest expected benefit from targeted retention campaigns.
- ROI analysis showed that targeting high-risk customers maximizes financial return while reducing unnecessary campaign costs.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- DoWhy

---

## Repository Structure

```
.
├── Telecom_Causal_Inference.ipynb
├── README.md
└── requirements.txt
```

---

## Future Improvements

- Incorporate real-world campaign data
- Apply uplift modeling for individualized treatment effects
- Explore Causal Forests and Double Machine Learning
- Develop an interactive dashboard for business users

---

## Author

**Sagnik Mukherjee**

B.Tech Computer Science Engineering

Thapar Institute of Engineering & Technology

---

## License

This project is intended for educational and research purposes.
