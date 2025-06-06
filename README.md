# Breast Cancer Detection Using Machine Learning

## Project Description

This project uses machine learning models to detect whether a breast mass is malignant (cancerous) or benign (non-cancerous) based on data from the **Wisconsin Breast Cancer Diagnostic** dataset. The goal is to support early and accurate cancer detection using reliable classification techniques.

## Who Will Benefit and Why?

* **Healthcare Professionals**: Can use ML-based tools to support early diagnosis, aiding faster decision-making.
* **Medical Researchers**: Gain insight into which cell characteristics are most strongly associated with malignancy.
* **Data Scientists in Health Tech**: Useful case study for implementing classification models in a biomedical context.
* **Students and Beginners in ML**: A beginner-friendly yet impactful application of ML in healthcare.

## Dataset

The dataset includes 569 samples of digitized images of breast cell nuclei, extracted from fine needle aspirates. Each sample includes 30 numeric features such as radius, texture, perimeter, and area, derived from the cell images.

* **Target Variable**:

  * `M` = Malignant
  * `B` = Benign
* **Distribution**:

  * 200 malignant cases
  * 350 benign cases
  * Indicates moderate class imbalance

---

## Approach

### Data Preparation

* Diagnosis values were mapped numerically for modeling, then converted back to labels for visualization.
* Features were standardized before training models to improve convergence and accuracy.

### Correlation Analysis

* Identified top features most associated with cancer:

  * **Positive correlation**: `concavity_worst`, `radius_mean`
  * **Negative correlation**: `area_se`
* A full **correlation matrix** was created to visualize relationships across features.

---

## Machine Learning Models Used

### 1. Logistic Regression

* **Accuracy**: 96.49%
* **Precision/Recall/F1**: 0.957 each
* **Cross-validation Accuracy**: 97.81%
* Strong baseline model with balanced performance

### 2. Random Forest Classifier

* **Accuracy**: 96.49%
* **Precision**: 0.939
* **Recall**: 0.979
* **F1 Score**: 0.958
* Performed similarly to Logistic Regression, with higher recall

### 3. XGBoost Classifier

* **Accuracy**: 95.61%
* **Precision**: 0.938
* **Recall**: 0.957
* **F1 Score**: 0.947
* Competitive performance, slightly behind other models

### Final Logistic Regression Model (after hyperparameter tuning)

* Maintained **96.49% accuracy** and **0.957 precision/recall/F1 score**
* Final model used for single observation testing

---

## Single Observation Analysis

* A new observation was processed and fed into the final model
* **Result**: Classified as **malignant**
* Demonstrated the model’s practical use for real-time prediction

---

## Key Findings

* Logistic Regression and Random Forest are highly accurate for this task
* Features like **concavity** and **radius** are strong indicators of malignancy
* Class imbalance exists but models still performed well
* Logistic Regression provided the best balance of accuracy and simplicity

---

## Conclusion

This project shows that machine learning models, especially Logistic Regression and Random Forest, can effectively classify breast tumors as malignant or benign with high accuracy. These models offer potential for integration into diagnostic tools to support healthcare professionals.

---

## Acknowledgment

This project was developed using material from the Udemy course:
**“Machine Learning Projects for Beginners in Python” by John Bura**
[Course Link](https://www.udemy.com/course/machine-learning-projects-for-beginners-in-python/learn/lecture/31593632?start=1#reviews)

