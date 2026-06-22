# Fraud Alert Prioritization & Investigator Control Tower

## Overview

Fraud teams don't just need to detect suspicious transactions—they need to decide which alerts deserve attention first.

This project simulates a fraud analytics team working in a banking environment. The goal is to build a system that identifies potentially fraudulent transactions, prioritizes them based on risk, and provides investigators with clear explanations and operational insights.

The project combines machine learning, fraud analytics, explainability, and dashboarding to demonstrate how data science can support real-world fraud operations.

---

## Business Problem

Fraud investigation teams face three common challenges:

* Large volumes of alerts
* High false-positive rates
* Limited investigator capacity

Reviewing every alert is expensive and inefficient. Missing genuine fraud can result in financial loss and customer impact.

The objective of this project is to help investigators focus on the highest-risk transactions while maintaining transparency around why alerts were generated.

---

## Dataset

The project uses synthetic banking data consisting of:

* Customer profiles
* Merchant information
* Transaction activity
* Alert queue records

The dataset includes behavioral, geographic, device, merchant, and account-level risk signals that are commonly used in fraud detection systems.

---

## Approach

### 1. Data Preparation

The customer, merchant, and transaction datasets were merged into a single analytical dataset.

Several data quality checks were performed, including:

* Missing value analysis
* Duplicate feature detection
* Feature validation
* Risk signal verification

---

### 2. Feature Engineering

Features were created to capture suspicious behavior patterns, including:

* Cross-border transactions
* High-value transactions
* Night-time activity
* New device usage
* Transaction velocity
* Device risk indicators
* Merchant risk indicators
* Customer KYC risk bands

Each engineered feature was validated against fraud outcomes before being included in the model.

---

### 3. Fraud Risk Modeling

A supervised machine learning model was trained to predict the likelihood of fraud.

Model evaluation focused on operational usefulness rather than accuracy alone.

Metrics included:

* ROC-AUC
* Precision
* Recall
* F1 Score
* Threshold analysis
* Confusion matrix evaluation

---

### 4. Alert Prioritization

Every transaction receives a fraud risk score.

Transactions are assigned to one of three investigation tiers:

| Tier   | Description                  |
| ------ | ---------------------------- |
| High   | Immediate review required    |
| Medium | Standard investigation queue |
| Low    | Monitor only                 |

This allows investigator resources to be directed toward the highest-risk cases.

---

### 5. Explainability

To support analyst decision-making, model predictions are accompanied by explanation outputs showing which factors contributed most to a transaction's risk score.

Example risk drivers include:

* Elevated device risk
* Cross-border activity
* High transaction velocity
* High-risk merchants
* New device usage

---

## Dashboard

A Power BI dashboard was designed to provide operational visibility into fraud investigations.

Key metrics include:

* Alert volume
* Fraud hit rate
* False-positive rate
* Queue size
* Priority distribution
* SLA performance
* Investigation outcomes

The dashboard is intended to support fraud operations managers in monitoring team performance and investigation workload.

---

## Key Learnings

This project reinforced that successful fraud analytics is not only about building predictive models.

The biggest challenge is balancing fraud detection performance with operational realities such as investigator capacity, explainability requirements, governance expectations, and alert fatigue.

---

## Tools Used

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* SHAP
* SQL
* Power BI

---

## Future Improvements

Potential extensions include:

* Cost-sensitive threshold optimization
* Real-time transaction scoring
* Investigator staffing simulations
* Champion–challenger model monitoring
* Streamlit case-review application

---

## Author

This project was completed as a fraud analytics and machine learning capstone focused on combining predictive modeling with operational decision-making and responsible AI practices.
