# ML Fundamentals – Aviation Focus git add README.md
git commit -m "Add README for regression notebook"
git push


This repository contains hands-on machine learning projects developed as part of a structured
ML learning plan with an aviation and operations focus.

The goal is to build strong foundations in applied machine learning while emphasizing
realistic decision-making, model evaluation, and safety-critical considerations
relevant to industries such as aviation, energy, and industrial operations.

---

## Notebooks

### 01 – Regression: Energy Consumption Prediction
- Objective: Predict energy consumption for the following year using historical data
- Model: Linear Regression
- Key steps:
  - Data cleaning and preprocessing
  - Train/test split
  - Model evaluation (MSE, R²)
  - Residual analysis
- Notes:
  - Baseline regression model using prior-year consumption as the main feature
  - Focus on interpretability and error analysis

---

### 02 – Classification: Predictive Maintenance (Failure Detection)
- Objective: Predict machine failure events based on operational and sensor data
- Problem type: Binary classification with strong class imbalance
- Models:
  - Logistic Regression (baseline)
  - Random Forest Classifier (final model)
- Key steps:
  - Feature selection 
  - Encoding of categorical variables
  - Handling class imbalance
  - Evaluation using confusion matrices, precision, recall, and F1-score
  - Decision threshold tuning to prioritize failure recall
- Model selection rationale:
  - Recall for the failure class was prioritized over overall accuracy
  - False positives were considered acceptable to reduce missed failures
- Final results:
  - Recall (failure): ~77%
  - Precision (failure): ~61%
- Visualizations:
  - Confusion matrix heatmap
  - Precision–Recall curve
  - Feature importance analysis
- Notes:
  - The final model reflects realistic predictive maintenance trade-offs
  - Emphasis on safety-critical evaluation rather than accuracy alone

---

## Tech Stack
- Python
- pandas, numpy
- scikit-learn
- matplotlib, seaborn

---

## Status
- Notebook 01 completed
- Notebook 02 completed
- Notebook 03 (Anomaly Detection) planned

