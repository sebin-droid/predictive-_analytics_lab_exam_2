# predictive-_analytics_lab_exam_2
Classification task using Logistic Regression
# Predictive Analytics Lab Exam-2  
## Binary Classification using Logistic Regression

---

Objective
The objective of this lab exam is to perform a binary classification task using a suitable machine learning algorithm. The project includes:
- Exploratory Data Analysis (EDA)
- Building a classification model
- Visualizing the decision boundary
- Evaluating model performance

 Dataset Description

The dataset contains:
- **Feature1** (Numerical)
- **Feature2** (Numerical)
- **Target** (Yes / No)

Initial dataset size: **1020 rows**

After preprocessing:
- 20 rows with missing Target values removed
- 1 extreme outlier removed (Feature1 = 10000)

Final dataset size used for modelling: **999 samples**

 Exploratory Data Analysis (EDA)

The following EDA steps were performed:

Data Inspection
- Checked data types
- Generated summary statistics
- Identified missing values

Missing Values Handling
- Dropped rows with missing Target values

Outlier Detection
- Used IQR method for Feature1
- Removed extreme outlier (Feature1 = 10000)

Class Distribution
- No: 784 samples  
- Yes: 215 samples  
- Class imbalance ratio ≈ 3.65 : 1

Visualizations
- Class distribution bar plot
- Feature histograms + KDE
- Boxplots by class
- Scatter plot (Feature1 vs Feature2)
- Correlation heatmap

Correlation with Target
- Feature1 correlation: -0.044
- Feature2 correlation: -0.008

The features show **very weak correlation** with the target.



Model Building

Algorithm Used:
**Logistic Regression**

Why Logistic Regression?
- Suitable for binary classification
- Interpretable coefficients
- Provides probability outputs
- Allows decision boundary visualization

Preprocessing:
- Stratified 80/20 train-test split
- StandardScaler used (important due to feature scale differences)
- Class imbalance handled using `class_weight='balanced'`

---

Cross-Validation Results (5-Fold Stratified)

| Metric | Value |
|--------|-------|
| CV Accuracy | 0.5215 ± 0.0325 |
| CV ROC-AUC | 0.5279 ± 0.0267 |

Model performance is close to random (≈ 0.5), indicating weak feature-target relationship.

Decision Boundary

A decision boundary was plotted in the original feature space:

- Background shows predicted probability P(Yes)
- Black dashed line represents probability = 0.5 boundary
- Data points plotted with class labels

Observation:
The boundary is nearly linear and does not strongly separate classes, confirming weak predictive power.



Model Evaluation (Test Set)

| Metric | Value |
|--------|--------|
| Accuracy | 55.50% |
| Precision (Yes) | 0.2745 |
| Recall (Yes) | 0.6512 |
| F1-Score (Yes) | 0.3862 |
| ROC-AUC | 0.5392 |

### Confusion Matrix:

- True Negatives (TN): 83
- False Positives (FP): 74
- False Negatives (FN): 15
- True Positives (TP): 28

---

Interpretation of Results

- Accuracy is slightly above random guessing (50%)
- ROC-AUC ≈ 0.54 → weak discriminative ability
- High recall for "Yes" but low precision
- Indicates model struggles due to weak feature relevance

---

Conclusion

- Logistic Regression was successfully implemented.
- Data preprocessing, scaling, cross-validation, and evaluation were properly performed.
- The features have very weak correlation with the target, limiting model performance.
- The decision boundary confirms limited class separability.

This implementation fully satisfies:

✔ Exploratory Data Analysis  
✔ Model Building  
✔ Decision Boundary Visualization  
✔ Performance Evaluation  

---



Libraries Used

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## 👨‍💻 Author

Predictive Analytics Lab – Exam 2  
Binary Classification Project
