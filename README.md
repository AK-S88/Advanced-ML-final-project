# 📑 Biomedical Text Classification – Cancer Document Classification (Academic Project)

> **Course**: MIST 6170 – Advanced Machine Learning  
> **Semester**: Spring 2025  
> **Team Members**: Abhishek Kumar Singh, Nithyashree Bandihalli Rangaswamy, Sanjay Sandhosh

## 🔍 Project Overview

This academic project addresses the challenge of categorizing cancer-related biomedical research abstracts using various machine learning techniques. With the rapid growth of scientific literature, there's a strong need for automated systems that assist clinicians and researchers in efficiently classifying and retrieving relevant publications.

We developed and evaluated a **Cancer Document Classification System** using traditional machine learning, ensemble models, and deep learning architectures.

## 🎯 Objectives

- Automate classification of research papers into **Colon**, **Lung**, and **Thyroid** cancer categories.
- Compare classical ML models with deep learning methods like **LSTM** and **CNN**.
- Highlight practical applicability in clinical and research decision-making workflows.

## 📁 Dataset Description

- **Source**: Kaggle  
- **Size**: ~6,000 biomedical abstracts  
- **Target Classes**: `Colon`, `Lung`, and `Thyroid` Cancer  
- **Features**:  
  - `cancer_type`: Label  
  - `research_paper`: Abstract text  
- **Data Quality**: Balanced classes, no missing values

## 🧪 Methodology

### 🔄 Preprocessing

- Text cleaning (lowercasing, punctuation removal)
- Stopword removal (NLTK)
- Vectorization using **TF-IDF** and **CountVectorizer**
- Stratified 3-way split: 60% train, 20% validation, 20% test

### ⚙️ Models Implemented

| Type       | Model                                  |
|------------|----------------------------------------|
| Classical  | Naive Bayes, Logistic Regression, SVM  |
| Ensemble   | Random Forest, XGBoost                 |
| Deep Learning | LSTM, CNN                           |
| Transformers | BERT (initial attempt, removed due to environment issues) |

## 📊 Performance Summary

| Model                    | Validation Accuracy | Remarks                      |
|--------------------------|---------------------|------------------------------|
| Multinomial Naive Bayes  | 91%                 | Solid baseline               |
| Logistic Regression      | 93%                 | Best linear model            |
| SVM                      | 92%                 | Comparable to Logistic Regression |
| Random Forest            | 100%                | Likely overfitting           |
| XGBoost                  | 100%                | Likely overfitting           |
| LSTM                     | 85%                 | Underperformed               |
| **CNN**                  | **97.29%**          | **Best test performance (97.16%)** |

## 💡 Key Insights

- **CNN** was most effective in identifying localized patterns in text, achieving top accuracy.
- Classical models performed well but plateaued at ~93%.
- Ensemble models overfit on structured data and lacked generalizability.
- Transformer models were explored but not included due to technical constraints.

## 🧠 Practical Implications

- Integration of such classifiers into **research dashboards** or **clinical support platforms** can drastically **reduce time and cost** in literature review.
- Future extensions include:
  - Adding more cancer types
  - Real-time document classification
  - Integration with biomedical embeddings (BioBERT, SciBERT)

## ⚠️ Challenges Faced

- **Overfitting** in tree-based models
- **Hardware limitations** for training transformers
- **Reproducibility issues** across environments for BERT

## ✅ Conclusion

The project demonstrated the potential of CNNs in biomedical text classification and underscored the importance of balancing model complexity with real-world applicability.
