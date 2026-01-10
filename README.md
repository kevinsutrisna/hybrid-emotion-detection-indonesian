# Hybrid Emotion Detection in Indonesian Music Comments
[![Status](https://img.shields.io/badge/Paper-Accepted-success)]() 
[![Conference](https://img.shields.io/badge/Index-Scopus-blue)]()
[![Dataset](https://img.shields.io/badge/Dataset-GitHub-orange)](https://github.com/kevinsutrisna/Emotion-Dataset/tree/main)

This repository contains the implementation of the research paper: **"Emotion Detection in Indonesian Music Comments Using BERT, Traditional Machine Learning and Their Hybrid Model"**. 

This study introduces a high-performance hybrid architecture that combines the contextual deep understanding of **IndoBERT** with the computational efficiency of **Traditional Machine Learning** to classify complex emotions in social media discourse.

---

## Research Overview
Detecting emotions in Indonesian music comments is challenging due to informal language, slang, and multilingual mixing. This project evaluates three paradigms:
1. **Traditional ML**: TF-IDF + SVD with algorithms like SVM, Random Forest, and XGBoost.
2. **Deep Learning**: Fine-tuned **IndoBERT** for end-to-end contextual classification.
3. **Hybrid Model**: Utilizing BERT as a feature extractor concatenated with TF-IDF, feeding into a traditional ML classifier.

---

## Methodology
The pipeline follows a rigorous process from manual data collection to model evaluation:

* **Data Collection**: 1,000 manually collected and labeled comments from YouTube and TikTok.
* **Emotion Labels**: Happiness, Sadness, Fear, Love, and Anger.
* **Feature Engineering**: TF-IDF vectors reduced via Singular Value Decomposition (SVD) and [CLS] token vector extraction from IndoBERT.


---

## Key Findings & Results
The research concludes that while pure BERT offers the highest accuracy, the **Hybrid (Logistic Regression + BERT)** model provides the best balance for production environments.

| Model Paradigm | Accuracy | Training Time | Memory Usage |
| :--- | :---: | :---: | :---: |
| **Traditional (SVM)** | 66% | **0.29 s** | **1,504 MiB** |
| **Pure IndoBERT** | **79%** | 335.95 s | 5,868 MiB |
| **Hybrid (LR + BERT)** | **77%** | **4.10 s** | 4,682 MiB |

**Key Takeaway**: The Hybrid approach (Logistic Regression + BERT) achieves **97% of BERT's accuracy** while being **~80x faster** in training.

---

## 🛠️ Implementation
The models were developed using:
- **Environment**: Google Colab (T4 GPU).
- **Libraries**: HuggingFace Transformers, Scikit-learn, Sastrawi (for Indonesian stemming).
