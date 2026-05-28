
---

# 🚨 Anti-Money Laundering Detection using Deep Learning

A deep learning-based **Anti-Money Laundering (AML)** detection system built using the **IBM AML transaction dataset**. This project leverages **PyTorch, behavioral feature engineering, and threshold optimization** to identify suspicious financial transactions in highly imbalanced banking data. Built from an end-to-end ML pipeline including EDA, feature engineering, model training, and evaluation. Based on your notebook analysis and results. 

## 📌 Problem Statement

Money laundering detection is a challenging **rare-event classification** problem.

Dataset statistics:

* **6.9M+ transactions**
* **3,565 laundering cases**
* **0.051% fraud rate**
* **1:1941 imbalance ratio**

The goal is to accurately identify laundering transactions while minimizing false positives.

---

## ⚙️ Pipeline

### Data Processing

* Data cleaning and EDA
* Class imbalance analysis
* Temporal transaction analysis
* Log transformation for transaction amounts

### Feature Engineering

* Time-based features
* Amount ratios and mismatch indicators
* Currency and payment format encoding
* Bank frequency encoding
* Account-level behavioral features

### Modeling

* PyTorch Feedforward Neural Network
* BCEWithLogitsLoss with class weighting
* Adam optimizer + LR scheduling
* Early stopping
* Threshold optimization

---

## 🧠 Model Architecture

```text
Input → 128 → 64 → 32 → Output
        ReLU + BatchNorm + Dropout
```

* 3 hidden layers
* Dropout regularization
* Batch normalization
* Binary classification output

---

## 📊 Results

| Metric    | Final Score |
| --------- | ----------: |
| ROC-AUC   |       0.969 |
| F1 Score  |       0.101 |
| Precision |       0.065 |
| Recall    |       0.229 |

### Key Findings

✅ Behavioral features improved detection significantly
✅ Threshold tuning improved F1 performance
✅ Strong ranking capability with ROC-AUC ≈ 0.97
⚠️ Extreme imbalance still causes false positives

Results summarized from the uploaded notebook report. 

---

## 🛠 Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* PyTorch
* Matplotlib
* Seaborn

---

## 📁 Project Structure

```bash
├── data/
├── notebooks/
├── models/
├── outputs/
└── README.md
```

---

## 🚀 Future Work

* Gradient boosting models (XGBoost/LightGBM)
* Anomaly detection methods
* Temporal transaction velocity features
* Graph Neural Networks for account relationships

---


