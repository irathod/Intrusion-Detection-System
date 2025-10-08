# 🧠 Intrusion Detection System using Random Forest

## 📘 Course Information
**Chaitanya Bharathi Institute of Technology (A)**  
**Department of Information Technology**  
**Programme:** B.E. (IT-1,2) Semester: V AY: 2025-26  
**Course:** Cyber Security (Course Code: 22CIE55)  
**Faculty:** U Sairam  

---

## 🎯 Project Overview
This repository contains the implementation of **Cyber Security Assignment 2**:  
**“Intrusion Detection System using Random Forest and Feature Selection on NSL-KDD Dataset.”**

The objective is to analyze network traffic data, detect potential intrusions, and improve model accuracy using **SMOTE oversampling** and **hyperparameter tuning**.

---

## 🧩 Problem Statement
- Network intrusion detection systems often suffer from **class imbalance**.
- The goal is to build a model that distinguishes between **normal** and **attack** network connections.
- This project uses **Random Forest Classifier** on the **NSL-KDD dataset** to detect anomalies.

---

## 📊 Dataset Description
- **Dataset Name:** NSL-KDD (Improved version of KDD Cup 1999)
- **Training Samples:** 125,973  
- **Testing Samples:** 22,544  
- **Features:** 41  
- **Target:** Binary classification  
  - `0` → Normal  
  - `1` → Attack  

**Source:** [NSL-KDD Dataset](https://www.unb.ca/cic/datasets/nsl.html)

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing
- Loaded `KDDTrain+.txt` and `KDDTest+.txt`
- Applied:
  - One-hot encoding for categorical columns (`protocol_type`, `service`, `flag`)
  - Standard scaling on numeric columns
  - Binary labeling for target

### 2️⃣ Baseline Model
- Trained a **Random Forest Classifier** on the raw dataset.
- Evaluated using classification metrics (Precision, Recall, F1-score, ROC AUC).

### 3️⃣ Model Improvement
- Applied **SMOTE** on a subset of the training data to handle class imbalance.
- Performed **RandomizedSearchCV** for hyperparameter tuning.
- Compared improved model performance against baseline.

---

## 🧠 Model Performance

| Metric | Baseline Random Forest | Improved Random Forest |
|--------|------------------------|-------------------------|
| Accuracy | 0.78 | 0.78 |
| ROC AUC | 0.9584 | 0.9614 |
| F1-Score (Attack) | 0.76 | 0.77 |

---

## 📈 Key Findings
- Applying SMOTE improved **recall and F1-score** for attack class.
- ROC AUC slightly increased from **0.958 → 0.961**, showing better generalization.
- The model is stable and effective for IDS baseline use.

---



## 🚀 How to Run
1. Open the Colab notebook: `IDS_Assignment2.ipynb`
2. Upload the NSL-KDD dataset files:
   - `KDDTrain+.txt`
   - `KDDTest+.txt`
3. Run all cells in order.
4. View the classification reports, ROC AUC, and confusion matrix in output.
5. (Optional) Update results and export the model using `joblib`.

---

## 📚 Technologies Used
- Python (Google Colab)
- Pandas, NumPy
- scikit-learn
- imbalanced-learn (SMOTE)
- Matplotlib, Seaborn

---

## 🧩 Conclusion
The experiment demonstrates how Random Forests combined with resampling and tuning can effectively classify normal vs. attack network traffic.  
This project provides a baseline framework for building **AI-powered Intrusion Detection Systems** in cybersecurity applications.

---

## 👨‍💻 Author
**Name:** K.Manmohan Rathod  
**Roll No:** 160123737044  
**Section:** IT-1 
**Date:** 08/10/2025

---

## 🏫 Acknowledgment
This project is part of the Cyber Security Course (22CIE55) under the guidance of **U Sairam**, Department of Information Technology, **CBIT (A)**.

