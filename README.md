# Credit-Risk-IRB-Modeling-System
This project implements a complete Internal Ratings-Based (IRB) modeling system for credit risk assessment, following Basel III regulatory standards. The system estimates Probability of Default (PD) and Loss Given Default (LGD) while emphasizing model explainability, fairness auditing, and regulatory compliance.

## Dataset

Source: UCI Machine Learning Repository - Statlog (German Credit Data)

- 1000 credit applications with 20 features
- Binary target: Good vs. Bad credit risk
- Mixed data types: categorical, ordinal, and numerical features

Key Transformations:

- German feature names translated to English
- Age grouping for fairness analysis
- LGD simulation for modeling completeness

## Key Results

**Model Performance**
- PD Model AUC: 0.729 - 0.737
- LGD Model R²: -0.005 (highlighting need for actual recovery data)
- Demographic Parity Difference: 0.240 - 0.321 (requires mitigation)

**Portfolio Insights**
- Total Expected Loss: €1.24M
- Regulatory Capital Requirement: €1.32M (40.32% of portfolio)
- Stress Test Impact: +46% EL under adverse conditions

**Business Implications**
- Concentration Risk: 60% of EL from single job category
- Profitability Challenge: Negative expected returns across segments
- Pricing Strategy: Current rates may be insufficient for risk profile

### Regulatory Compliance

This framework addresses key Basel III requirements:

- PD Model Validation: Cross-validation and performance benchmarking
- LGD Model Development: Multiple modeling approaches
- Stress Testing: Economic downturn scenarios
- Concentration Risk: Portfolio segmentation analysis
- Model Documentation: Transparent and auditable process
- Fairness Compliance: Bias detected - requires mitigation strategies

## Key Features

**Risk Modeling**

- PD Estimation: Logistic Regression models with feature importance analysis
- LGD Modeling: Multiple approaches (Linear Regression, Random Forest)
- Expected Loss Calculation: Basel-compliant EL = PD × LGD × EAD
- Portfolio Risk Assessment: Concentration analysis and sensitivity testing

**Fairness & Ethics**

- Bias Detection: Demographic Parity and Equalized Odds analysis
- Pre-modeling Fairness Audit: Identifying inherent dataset biases
- Proxy Variable Analysis: Detecting potential discriminatory features
- Model Comparison: Fair vs. full feature set performance

**Explainability**

- SHAP Analysis: Global and local feature importance
- Model Interpretability: Transparent decision-making process
- Regulatory Documentation: Audit-ready model documentation

## Limitations & Future Work

**Current Limitations**

- LGD Modeling: Simulated data (no actual recovery history)
- Feature Set: Limited to available variables in dataset
- Model Complexity: Basic algorithms for interpretability

## Data Source

[UCI Machine Learning Repository - Statlog (German Credit Data)](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data)
