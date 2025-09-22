# 👶 Fetal Health – Multi-Class Classification (with XAI)

End-to-end pipeline to classify fetal health into **three classes** — **Normal**, **Suspect**, **Pathological** — from tabular CTG-derived features.  
The workflow covers robust preprocessing, model training, **class-imbalance handling (ADASYN)**, rigorous evaluation, and **explainability** with **SHAP** and **LIME**.

---

## 🧭 Overview

We build reliable multi-class models to predict fetal health status from clinical/tabular features.  
Two complementary notebooks are provided:

- **`Fetal_health_multiclass_classification.ipynb`** – baseline pipeline (no ADASYN).  
- **`Fetal_health_multiclass_classification_adasyn.ipynb`** – same pipeline with **ADASYN** oversampling for class balance.

---

## 🔄 Pipeline

1. **EDA**: overview of distributions and target imbalance.  
2. **Multicollinearity**: correlation heatmap (optionally VIF).  
3. **Missing values**: check & imputation (e.g., median for skewed features).  
4. **Outliers**: inspection and robust handling.  
5. **Feature selection**: **Mutual Information** for dimensionality reduction.  
6. **Encoding**: **target encoding** for categorical variables.  
7. **Scaling**: **RobustScaler** (resistant to outliers).  
8. **Class imbalance**: **ADASYN** oversampling (variant notebook).  
9. **Modeling**: train several ML models for multi-class classification.  
10. **Persistence**: save the trained model and preprocessing objects.  
11. **Evaluation**: confusion matrix, per-class Precision/Recall/F1, macro/micro averages, ROC-AUC (OvR).  
12. **Explainability (XAI)**:  
    - **SHAP** (global feature importance + local explanations)  
    - **LIME** (local instance-level reasoning)

---

## 📂 Repository Structure
```
Fetal_Health_Multi-Class_Classification-with-XAI/
├── Fetal_health_multiclass_classification.ipynb
├── Fetal_health_multiclass_classification_adasyn.ipynb
├── requirements.txt
└── README.md
```



---

## ⚙️ Setup

Install dependencies:

```bash
pip install -r requirements.txt
