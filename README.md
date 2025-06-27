# task4
# 🧠 Breast Cancer Detection using Logistic Regression

This project uses **Logistic Regression** to predict whether a tumor is **Malignant (M)** or **Benign (B)** using the **Breast Cancer Wisconsin dataset**. It also includes **ROC-AUC analysis** and **custom threshold tuning** to improve medical diagnosis sensitivity.

---

## 🚀 Key Features

- Logistic Regression classifier
- Sigmoid function for probability output
- ROC Curve and AUC evaluation
- **Custom threshold tuning** to improve recall
- Confusion Matrix with Seaborn heatmap
- Plots ROC curve and highlights best threshold

---

## 📊 Dataset

- Source: [UCI Breast Cancer Wisconsin (Diagnostic) dataset](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
- Target: `diagnosis` column (`M` for malignant, `B` for benign)

---

## 📈 Model Evaluation

- ROC Curve and AUC are used to evaluate the classifier
- Threshold is manually tuned to maximize **recall**
- Custom predictions are made using:
  ```python
  y_pred_tuned = np.where(prob_x[:, 1] >= best_threshold, 'M', 'B')
