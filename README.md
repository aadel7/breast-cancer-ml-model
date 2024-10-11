# Breast Cancer Classification Model

## Problem Definition
Breast cancer is a major health concern worldwide, and early detection is key to improving outcomes. This project aims to build a machine learning model to accurately classify breast tumors as benign or malignant, based on features extracted from digitized images.

## Dataset
### Wisconsin Diagnostic Breast Cancer Dataset
- **Features**: 30 numeric variables related to the characteristics of the cell nuclei.
- **Target**: Binary classification - `M` (Malignant) and `B` (Benign).
- The dataset contains 569 instances, and each tumor sample has 10 features, including:
  - Radius (mean of distances from center to points on the perimeter)
  - Texture (standard deviation of gray-scale values)
  - Perimeter
  - Area
  - Smoothness (local variation in radius lengths)
  - Compactness (perimeter^2 / area - 1.0)
  - Concavity (severity of concave portions of the contour)
  - Concave points (number of concave portions of the contour)
  - Symmetry
  - Fractal dimension ("coastline approximation" - 1)

## Data Preprocessing
- **Handling Target Variable**: The target labels (`M` and `B`) were mapped to binary values.
- **Data Standardization**: Applied `StandardScaler` to standardize the feature values.
- **Feature Selection**: Random Forest Classifier was used to determine the most important features.

## Feature Engineering & Dimensionality Reduction
- **Top Features**: Features like `area`, `concavity`, and `perimeter` were identified as the most significant predictors.
- **Principal Component Analysis (PCA)**: Applied PCA to reduce dimensionality while preserving 95% of the variance. Used the first 5 principal components for model training.

## Model Building
### Algorithms Used:
- **Logistic Regression**
- **Decision Tree Classifier**
- **Random Forest Classifier**
- **Support Vector Machine (SVM)**
- **k-Nearest Neighbors (KNN)**
- **Neural Network**

### Model Selection
- **Cross-Validation**: K-Fold Cross-Validation was performed to estimate model performance.
- **Best Performers**: Logistic Regression and SVM were the best models based on accuracy and F1-Score.

## Results
- **Logistic Regression**: Achieved an accuracy of **98%** and an F1-Score of **0.99 (Benign)** and **0.98 (Malignant)**.
- **Neural Network**: Achieved an accuracy of **96%**, with a slight trade-off in precision and recall for malignant cases.

## Conclusion
Both models performed exceptionally well, but Logistic Regression slightly outperformed with higher accuracy and better balance between precision and recall for both classes. The model's simplicity and performance make it the preferred choice for this classification task.
