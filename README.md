# ML Fundamentals – Aviation Focus

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
  - Feature selection and prevention of data leakage
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
  - ROC curve
  - Feature importance analysis
- Notes:
  - The final model reflects realistic predictive maintenance trade-offs
  - Emphasis on safety-critical evaluation rather than accuracy alone


---

### 03 – Anomaly Detection: Unsupervised Failure Detection
- Objective: Detect anomalous machine operating conditions without using failure labels
- Problem type: Unsupervised anomaly detection
- Model:
  - Isolation Forest
- Key steps:
  - Feature selection using only sensor and operational variables
  - Training on non-failure (healthy) data only
  - Anomaly scoring and binary anomaly labeling
  - Comparison of detected anomalies with true failure labels
- Evaluation:
  - Confusion matrix against `Machine failure`
  - Precision, recall, and F1-score for anomaly detection
- Key observations:
  - The model accurately learns normal operating behavior
  - Only a subset of failures are detected as anomalies
  - Not all failures are statistically abnormal
- Notes:
  - This notebook demonstrates the limitations and strengths of unsupervised detection
  - Anomaly detection is positioned as an early warning or complementary system
    rather than a standalone failure predictor


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
- Notebook 03 completed
- Hybrid predictive maintenance approach planned



---

## Project Summary

This repository presents a structured set of machine learning projects focused on
predictive maintenance and operational analytics, inspired by challenges common
in aviation and industrial systems.

The project progresses from simple, interpretable models to more advanced and
realistic machine learning approaches, emphasizing correct evaluation, avoidance
of data leakage, and safety-critical decision-making.

### Key Outcomes

- **Regression (Notebook 01):**
  - Built a baseline forecasting model for energy consumption
  - Emphasized interpretability, residual analysis, and error metrics
  - Established a foundation for data preprocessing and model evaluation

- **Supervised Classification (Notebook 02):**
  - Developed a predictive maintenance model for machine failure detection
  - Addressed class imbalance and misleading accuracy metrics
  - Optimized recall for failure events using threshold tuning and class weighting
  - Selected a Random Forest classifier as the final model
  - Achieved strong failure recall while maintaining acceptable precision

- **Unsupervised Anomaly Detection (Notebook 03):**
  - Applied Isolation Forest to detect anomalous operating conditions without labels
  - Trained exclusively on normal(no-failure) data to model normal behavior
  - Demonstrated that not all failures are statistically anomalous
  - Positioned anomaly detection as an early warning or complementary system

### Key Insights

- High accuracy alone is insufficient in safety-critical systems
- Recall for rare but critical events must be prioritized
- Supervised and unsupervised methods serve different but complementary roles
- A hybrid approach provides robustness to unknown failure modes

### Future Work

- Hybrid predictive maintenance combining anomaly detection and classification
- Time-series and sequential modeling for early failure detection
- Risk-based decision thresholds for maintenance planning

This project reflects a realistic, engineering-oriented approach to applied
machine learning, aligned with industry practices in aviation and operations.


