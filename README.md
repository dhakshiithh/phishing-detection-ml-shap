# 🛡️ Phishing Website Detection using Machine Learning

This project implements an end-to-end **phishing detection pipeline** leveraging multiple machine learning algorithms to classify URLs as legitimate or phishing based on extracted features.

---

## 📂 **Dataset**

- **Source**: [Kaggle - Web Page Phishing Detection Dataset](https://www.kaggle.com/datasets)  
- **Size**: ~48 engineered features per URL

---

## ⚙️ **Project Pipeline**

1. **Data Cleaning**
   - Removed missing values.
   - Encoded target labels (phishing=1, legitimate=0).

2. **Feature Engineering**
   - Correlation-based feature selection with **threshold > 0.2**, reducing dimensionality significantly.

3. **Preprocessing**
   - Standardised features using **StandardScaler**.

4. **Model Training & Tuning**
   - Trained and hyperparameter tuned:
     - Logistic Regression
     - Random Forest
     - Gradient Boosting
     - SVM
     - KNN
   - Used **GridSearchCV (5-fold)** for optimal parameters.

5. **Evaluation**
   - Computed accuracy, precision, recall, confusion matrix, and classification report for each model.
   - **Achieved ~98% test accuracy** using Random Forest.

6. **Model Interpretability**
   - Implemented SHAP analysis to interpret feature importances over 1000 samples.

7. **Deployment**
   - Saved trained Random Forest model and scaler using **pickle** for future integration.

---

## 📊 **Key Results**

| Model                | Best Test Accuracy |
|-----------------------|---------------------|
| Random Forest        | ~98.2%             |
| Gradient Boosting    | ~97.8%             |
| SVM                  | ~96.5%             |
| Logistic Regression  | ~95.3%             |
| KNN                  | ~93.1%             |

---

## 💡 **Future Work**

- Integrate into a **Flask web application** for real-time URL scanning  
- Expand dataset with live phishing data feeds  
- Explore ensemble stacking for improved generalisation

---

## 🧑‍💻 **Author**

[Your Name]

---

> ⚠️ **Note**: Replace placeholder accuracies with final results from your notebook before publishing.
