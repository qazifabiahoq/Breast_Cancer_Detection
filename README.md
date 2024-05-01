# Breast Cancer Detection Analysis

This repository contains code for training machine learning models to detect breast cancer using the Wisconsin Breast Cancer dataset. The dataset contains features computed from digitized images of fine needle aspirates of breast masses, and the target variable indicates whether the mass is malignant (M) or benign (B).

## Analysis Overview

### Data Mapping and Distribution:
Mapping Diagnosis Values: Diagnosis values were encoded and mapped back to 'M' (malignant) and 'B' (benign) for analysis.
Diagnosis Distribution: The dataset contains 569 instances, with 200 malignant cases and 350 benign cases, indicating an imbalance.

### Correlation Analysis:
Correlation with Diagnosis (Malignant): Features were correlated with the diagnosis to identify relationships. For instance, 'area_se' showed a negative correlation with malignant diagnoses.
Correlation Matrix: A correlation matrix was created to visualize relationships between features. Features like 'concavity_worst' showed a strong positive correlation with malignant diagnoses.

### Model Training and Evaluation:
Logistic Regression: Achieved an accuracy of 96.49%, with a precision, recall, and F1 score of 0.957. Cross-validation showed an accuracy of 97.81%.
Random Forest Classifier: Achieved an accuracy of 96.49%, with a precision of 0.939, recall of 0.979, and F1 score of 0.958. Performance was comparable to Logistic Regression.
XGBoost Classifier: Achieved an accuracy of 95.61%, with a precision of 0.938, recall of 0.957, and F1 score of 0.947. Showed competitive performance with other models.
Final Logistic Regression Model: After hyperparameter tuning, achieved an accuracy, precision, recall, and F1 score of 96.49% and 0.957, respectively. Performed comparably to initial Logistic Regression and Random Forest models.

### Single Observation Analysis:
Preparation: The observation was standardized and shaped to match the training data.
Prediction: Classified as malignant (1) by the final Logistic Regression model.

## Conclusion

The analysis demonstrates the effectiveness of machine learning models, particularly Logistic Regression and Random Forest, for breast cancer detection. Further optimization and tuning could enhance performance, making these models valuable for clinical applications. The code and analysis can be used to understand and implement similar machine learning tasks in healthcare and medical research.
