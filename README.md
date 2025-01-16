# Convolve 3.0: Credit Card Default Prediction Model

## Team CKMKB, IIT Madras  
```
Atharva Kulkarni
Ayushmaan Pattnayak
Purandhar V
```

---

## 📑 Project Overview

This repository contains the framework for developing a **Behaviour Score** predictive model to assess credit card default probabilities among customers of Bank A. The project explores two approaches:

1. **Optimal Solution**: 
   - Employs **Artificial Neural Networks (ANNs)** for superior classification performance.
2. **Sub-optimal Solution**: 
   - Utilizes traditional machine learning classifiers on a PCA-transformed dataset, with **CatBoost** emerging as the top performer.

---

## 📂 Contents
- **Dataset and Preprocessing**
  - Data overview and handling missing values.
  - Dimensionality reduction using PCA.
  - Class imbalance correction with ADASYN.
- **Model Development**
  - Optimal Solution: ANN-based classification.
  - Sub-optimal Solution: Evaluation of classifiers including Decision Tree, Random Forest, Naive Bayes, XGBoost, CatBoost, and GBM.
- **Conclusions and Future Scope**
  - Key insights from preprocessing and model evaluation.
  - Future opportunities for ensemble methods and hyperparameter tuning.

---

## 📊 Dataset and Preprocessing
- **Dataset Overview**:
  - Contains **96,806 credit card records** for training (development dataset) and **41,792 records** for validation.
  - Attributes grouped into categories: On-us, Transaction-level, Bureau Tradeline, and Bureau Enquiry.
  - Target variable: `bad_flag` (`1` for defaults, `0` for non-defaults).

- **Preprocessing Steps**:
  - **Handling Missing Values**:
    - High-correlation features imputed using **autoencoder-based methods**.
    - Low-correlation features filled with default values (`0`).
  - **Dimensionality Reduction**:
    - Applied **PCA** to reduce features from over 1,200 to 176 components, retaining 80% variance.
  - **Class Imbalance**:
    - Addressed using **ADASYN**, ensuring a balanced dataset for effective training.

---

## 🔍 Model Development

### Optimal Solution
- **Architecture**:
  - Multi-layer ANN built using Keras with ReLU activation and Dropout layers for regularization.
  - Output layer with sigmoid activation for binary classification.
- **Performance**:
  - Achieved **ROC-AUC: 0.9427** and high accuracy, but interpretability remains a limitation.

### Sub-optimal Solution
- **Classifiers Evaluated**:
  - **Decision Tree**: Basic interpretable model, but limited by lower PR-AUC.
  - **Random Forest**: Improved performance with ensemble averaging.
  - **Naive Bayes**: Suboptimal due to strong assumptions.
  - **XGBoost**: Strong performance with recall and ROC-AUC.
  - **CatBoost**: Top performer among traditional models with **ROC-AUC: 0.92** and **PR-AUC: 0.33**.
  - **Gradient Boosting Machine (GBM)**: Competitive, but slightly outperformed by CatBoost.

---

## 📌 Key Conclusions
1. **Tree-based Models for Business Relevance**:
   - Models like CatBoost offer high interpretability, making them ideal for financial risk management.
2. **Neural Networks’ Predictive Power**:
   - While ANNs achieved the best results, they lack interpretability compared to tree-based models.
3. **Preprocessing Impact**:
   - Autoencoder-based imputation, PCA, and ADASYN significantly improved data quality and model performance.

---

## 🚀 Future Scope
1. **Incorporating Ensemble Methods and LSTMs**:
   - Explore combining LSTM networks with ensemble techniques for leveraging temporal patterns in data.
   - Weighted averaging of outputs can improve model accuracy and generalizability.
2. **Hyperparameter Tuning**:
   - Focus on fine-tuning CatBoost for better PR-AUC and ROC-AUC scores.
   - Despite computational expense, this could yield significant improvements for imbalanced datasets.

---

## 🔗 References
- [Comprehensive Overview of Big Data: Applications, Networking Technologies, and Challenges (IEEE)](https://ieeexplore.ieee.org/document/7727770)

For more details, [click here](https://github.com/atharvakulkarni-07/convolve_3.0) to access the solution CSV and other resources.

---

## 💻 Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/atharvakulkarni-07/convolve_3.0.git
  
---

### How to Use
1. Save this content in a file named `README.md`.
2. Add it to your GitHub repository root directory.
3. Push the changes to GitHub to display the README.
