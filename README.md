# 🧠 AutismNetX: Screening of Autism through Machine Learning

AutismNetX is a scalable, interpretable, and high-accuracy screening tool for Autism Spectrum Disorder (ASD). By combining advanced supervised learning algorithms (XGBoost, Gradient Boosting, Neural Networks) with Explainable AI and imbalance-handling techniques (SMOTE), it delivers rapid, data-driven early detection using demographic, behavioral, and clinical features.

| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| **AutismNetX (XGBoost + NN)** | 97.05%   | 0.96      | 0.98   | 0.97     |
| Neural Network      | 96.2%    | 0.95      | 0.97   | 0.96     |
| Random Forest       | 94.8%    | 0.93      | 0.95   | 0.94     |
---
![image](https://github.com/user-attachments/assets/4ecd2c05-3863-4652-ae16-ea3835c9c421)

## 📌 Table of Contents

- [Project Overview](#project-overview)  
- [Key Features & Objectives](#key-features--objectives)  
- [Motivation](#motivation)  
- [Dataset](#dataset)  
- [Methodology](#methodology)  
  - [1. Data Preprocessing](#1-data-preprocessing)  
  - [2. Feature Engineering](#2-feature-engineering)  
  - [3. Model Training & Optimization](#3-model-training--optimization)  
  - [4. Evaluation & Metrics](#4-evaluation--metrics)  
- [Results](#results)  
- [Future Scope](#future-scope)  
- [Installation & Usage](#installation--usage)  

---

## Project Overview

Autism Spectrum Disorder is a complex neurodevelopmental condition affecting social interaction, communication, and behavior. Traditional screening methods rely on expert evaluation and can be slow or subjective. AutismNetX offers:

- **Automated, scalable screening** using structured questionnaire and demographic data  
- **High accuracy** (~97% classification accuracy) on unseen test sets  
- **Interpretable predictions** via SHAP-based feature importance  
- **Adaptable framework** for clinics, schools, and home environments  

---

## Key Features & Objectives

1. **Predictive Modeling**  
   - Use supervised ML to classify ASD vs. non-ASD  
   - Incorporate Autism Quotient (AQ) scores (A1–A10)

2. **Imbalance Handling**  
   - Apply SMOTE to synthesize minority-class samples  
   - Optimize for precision, recall, and F1-score  

3. **Explainable AI**  
   - Generate SHAP explanations for model transparency  
   - Identify top predictive features (e.g., AQ questions A4, A5, A8)

4. **Scalable & Generalizable**  
   - Hybrid architectures: XGBoost, LightGBM, Neural Networks  
   - Cross-validation (K-Fold) and hyperparameter tuning  

5. **Ethics & Privacy**  
   - Secure handling of sensitive data  
   - Mitigate misclassification risks (false positives/negatives)

---
![image](https://github.com/user-attachments/assets/5228fa7f-b330-41f3-931d-da92a21393eb)

## Motivation

- **Early Intervention:** Timely ASD detection can dramatically improve long-term outcomes.  
- **Resource Efficiency:** Automated screening reduces dependence on specialist availability.  
- **Clinical Trust:** Explainable AI fosters adoption in healthcare settings.  
![image](https://github.com/user-attachments/assets/1d6dbb7b-8087-4d0b-9e74-51dc9ce9630b)

---

## Dataset

- **Source:** UCI “Autism Screening Adult Dataset”  
- **Features:**  
  - Demographics: Age, gender, ethnicity, country  
  - AQ Questionnaire responses (A1–A10)  
  - Family history, relationship status, screening results  
- **Target:** Binary `Class/ASD` label (Yes/No)

---

## Methodology

### 1. Data Preprocessing

- **Missing Value Imputation:** Mean/mode replacement or KNN imputation  
- **Normalization & Encoding:** Min–Max scaling; one-hot / label encoding  
- **SMOTE:** Synthetic Minority Over-sampling to balance classes  

### 2. Feature Engineering

- **Domain-driven aggregations:** Combine related questionnaire items  
- **Synthetic Augmentation:** Noise injection and bootstrapping for generalization  

### 3. Model Training & Optimization

- **Algorithms:**  
  - **Ensemble:** XGBoost, LightGBM, Random Forest  
  - **Deep Learning:** Fully-connected Neural Networks (ReLU activations)  
- **Validation:** 5-Fold Cross-Validation  
- **Hyperparameter Tuning:** Grid Search / Bayesian Optimization  

### 4. Evaluation & Metrics

- **Accuracy:** Overall correctness  
- **Precision & Recall:** Focus on sensitivity to ASD cases  
- **F1-Score:** Balance between precision and recall  
- **ROC-AUC & Confusion Matrix:** Discrimination ability and error analysis  

---

## Results

| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| **AutismNetX (XGBoost + NN)** | 97.05%   | 0.96      | 0.98   | 0.97     |
| Neural Network      | 96.2%    | 0.95      | 0.97   | 0.96     |
| Random Forest       | 94.8%    | 0.93      | 0.95   | 0.94     |

- **Top Predictive Features:** AQ questions A4, A5, A8  
- **Explainability:** SHAP summary plots demonstrate each feature’s impact on predictions  
![image](https://github.com/user-attachments/assets/5f281876-acc8-44df-9ea4-726042bf7283)
![image](https://github.com/user-attachments/assets/a2cc2b97-6390-4bb0-b9a8-4b3d6f7bffac)
![image](https://github.com/user-attachments/assets/20471a12-a26c-4370-8d9b-4ccdf7583bd5)
![image](https://github.com/user-attachments/assets/a05ba81f-6b62-4e11-b1d6-9e73b0e44dee)


---

## Future Scope

1. **Clinical Integration:** Deploy via APIs into EHR systems (HIPAA-compliant)  
2. **Multimodal Learning:** Incorporate audio, video, and neuroimaging data  
3. **Adaptive Screening:** Personalized models based on age, comorbidities  
4. **Federated & Transfer Learning:** Enhance generalization across institutions  
5. **Longitudinal Monitoring:** Continuous ASD risk tracking and intervention alerts  
6. **Global Adaptation:** Multilingual interfaces and culturally tailored questionnaires  

---


## Installation & Usage

1. **Clone the repo**  
   ```bash
   git clone https://github.com/Nagarjun-07/AutismNetX.git
   cd AutismNetX
