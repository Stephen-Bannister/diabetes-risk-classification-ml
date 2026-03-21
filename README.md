# Predicting Diabetes Risk Using Machine Learning

## Overview

This project develops and evaluates machine learning models to predict diabetes risk using patient health data. The work goes beyond basic modelling by incorporating interpretability, fairness analysis, and deployment considerations, reflecting real-world machine learning practice.

## Problem Statement

Early identification of diabetes risk can support preventative healthcare interventions.
The objective of this project is to build and compare classification models that predict diabetes outcomes based on patient health indicators, while balancing predictive performance, interpretability, and fairness.

---

## Dataset

The dataset consists of structured patient health data including:

* Glucose levels
* BMI (Body Mass Index)
* Age
* Insulin levels
* Blood pressure
* Other diagnostic measurements

The target variable indicates whether a patient is likely to have diabetes.

---

## Approach

### Data Preparation

* Identified and handled missing or invalid values (e.g. zero values in medical features)
* Analysed feature distributions and addressed skew and outliers
* Performed exploratory data analysis to understand relationships between variables

### Feature Analysis

* Used correlation analysis to identify predictive signals
* Reviewed feature redundancy and relevance
* Ensured features were suitable for modelling while avoiding over-reliance on correlation

### Model Development

Trained and evaluated multiple classification models, including:

* Logistic Regression
* Decision Tree
* Random Forest
* Gradient Boosting
* CatBoost
* Additional models for comparison

### Evaluation Metrics

* ROC AUC (primary metric)
* Precision and Recall
* Accuracy

ROC AUC was prioritised as it provides a balanced view of classification performance.

---

## Key Results

* **Best Performance:** Tree-based ensemble models (Random Forest and Gradient Boosting) achieved the highest ROC AUC (~0.76)
* **Interpretability:** Logistic Regression provided strong transparency into feature importance
* **Key Predictors:** Glucose, BMI, and age were the most influential features

### Trade-Off

* Ensemble models → higher accuracy
* Logistic Regression → better interpretability

This reflects a common real-world trade-off in machine learning systems.

---

## Model Interpretability

* Analysed Logistic Regression coefficients to understand feature impact
* Conducted local prediction analysis to explain individual outcomes
* Demonstrated how model predictions can be interpreted at both global and local levels

---

## Fairness Analysis

* Evaluated model performance across age and BMI groups
* Identified variation in error rates across demographic segments

**Insight:**
Model performance differences across groups indicate potential bias that would need to be addressed prior to deployment.

---

## Deployment Considerations

A conceptual deployment architecture was developed, including:

* Model serving layer
* Input validation
* Monitoring and logging
* Version control
* Retraining pipeline

This demonstrates how the model could be integrated into a real-world system.

---

## Model Drift Simulation

* Simulated changes in input data distributions
* Evaluated impact on model performance

**Insight:**
Even small shifts in data can degrade model performance, highlighting the need for monitoring and retraining in production systems.

---

## Model Validation

* Applied cross-validation to improve model robustness
* Performed hyperparameter tuning
* Explored additional modelling approaches (including TabNet for tabular deep learning)

---

## Technologies Used

* Python (pandas, NumPy)
* scikit-learn, PyTorch
* matplotlib, seaborn
* CatBoost
* Jupyter Notebook

---

## Repository Structure

```bash
├── notebooks/
│   └── diabetes_risk_prediction.ipynb
├── images/
│   └── correlation_heatmap.png
│   └── deployment_diagram.png
│   └── model_comparison.png
├── requirements.txt
└── README.md
```

---

## Key Learnings

* Importance of balancing accuracy and interpretability
* Need to evaluate fairness in machine learning models
* Real-world ML requires consideration of deployment and monitoring, not just model performance
* Data quality and preprocessing have a significant impact on outcomes

---

## Next Steps

* Validate model performance on external datasets
* Improve model calibration
* Extend fairness analysis across additional features
* Implement automated monitoring and retraining pipelines

---

## Author

Stephen Bannister

---

## Key References

* scikit-learn documentation
* Relevant machine learning and healthcare modelling resources
