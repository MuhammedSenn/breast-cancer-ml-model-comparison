# Breast Cancer ML Model Comparison

This work presents a comparative evaluation of several supervised machine learning algorithms using the **Breast Cancer Wisconsin Dataset**.  
The main objective is to classify tumors as **malignant (0)** or **benign (1)** based on quantitative diagnostic features.

## Models Included
- Logistic Regression  
- Random Forest  
- K-Nearest Neighbors (KNN)  
- Support Vector Classifier (RBF Kernel)  
- Decision Tree  

All models were trained using standardized feature inputs via `StandardScaler`, as consistent scaling helps improve optimization stability and distance-based classification performance.

## Evaluation Approach
To perform a fair comparison, the workflow uses:
- **Stratified Train/Test Split** to preserve class distribution
- **GridSearchCV** for systematic hyperparameter tuning
- **5-Fold Cross-Validation** to mitigate overfitting and estimate generalization performance
- **Test Accuracy** as the final performance metric on unseen data
- **Confusion Matrices** for analyzing prediction correctness and class misclassification

This methodology aims to provide a structured, reproducible, and balanced assessment of each model.

## Dataset Information
The dataset was loaded via `sklearn.datasets.load_breast_cancer` and consists of:
- **569 samples**
- **30 numeric diagnostic features**
- **Binary classification labels:**
  - `0`: malignant
  - `1`: benign  

The features represent statistical measurements computed from digitized tumor mass images.

## Notes
This project serves as a hands-on application of classical ML techniques within a medical classification context.  
It is not intended for clinical use or diagnostic decision-making.  
Model performance may vary depending on preprocessing strategies, cross-validation settings, or hyperparameter search ranges.

Suggestions, improvements, or further model extensions are always welcome.
