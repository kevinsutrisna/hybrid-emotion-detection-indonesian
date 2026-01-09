# 🎭 Hybrid Emotion Detection in Indonesian Music Comments

[![Status](https://img.shields.io/badge/Paper-Accepted-success)]() 
[![Conference](https://img.shields.io/badge/Index-Scopus-blue)]()
[![Dataset](https://img.shields.io/badge/Dataset-GitHub-orange)](https://github.com/kevinsutrisna/Emotion-Dataset/tree/main)

This repository contains the implementation of the research paper: **"Emotion Detection in Indonesian Music Comments Using BERT, Traditional Machine Learning and Their Hybrid Model"**. 

[cite_start]This study introduces a high-performance hybrid architecture that combines the contextual deep understanding of **IndoBERT** with the computational efficiency of **Traditional Machine Learning** to classify complex emotions in social media discourse[cite: 287, 294, 298].

---

## 📌 Research Overview
[cite_start]Detecting emotions in Indonesian music comments is challenging due to informal language, slang, and multilingual mixing[cite: 294, 316]. This project evaluates three paradigms:
1. [cite_start]**Traditional ML**: TF-IDF + SVD with algorithms like SVM, Random Forest, and XGBoost[cite: 294, 439].
2. [cite_start]**Deep Learning**: Fine-tuned **IndoBERT** for end-to-end contextual classification[cite: 442, 446].
3. [cite_start]**Hybrid Model**: Utilizing BERT as a feature extractor concatenated with TF-IDF, feeding into a traditional ML classifier[cite: 321, 447].

---

## 🏗️ Methodology
The pipeline follows a rigorous process from manual data collection to model evaluation:

* [cite_start]**Data Collection**: 1,000 manually collected and labeled comments from YouTube and TikTok[cite: 415, 418].
* [cite_start]**Emotion Labels**: Happiness, Sadness, Fear, Love, and Anger[cite: 420].
* [cite_start]**Feature Engineering**: TF-IDF vectors reduced via Singular Value Decomposition (SVD) and [CLS] token vector extraction from IndoBERT[cite: 426, 429, 430].


---

## 📊 Key Findings & Results
[cite_start]The research concludes that while pure BERT offers the highest accuracy, the **Hybrid (Logistic Regression + BERT)** model provides the best balance for production environments[cite: 497, 521].

| Model Paradigm | Accuracy | Training Time | Memory Usage |
| :--- | :---: | :---: | :---: |
| **Traditional (SVM)** | 66% | **0.29 s** | **1,504 MiB** |
| **Pure IndoBERT** | **79%** | 335.95 s | 5,868 MiB |
| **Hybrid (LR + BERT)** | **77%** | **4.10 s** | 4,682 MiB |

[cite_start]**Key Takeaway**: The Hybrid approach (Logistic Regression + BERT) achieves **97% of BERT's accuracy** while being **~80x faster** in training[cite: 474, 497, 507].

---

## 🛠️ Implementation
The models were developed using:
- [cite_start]**Environment**: Google Colab (T4 GPU)[cite: 435].
- [cite_start]**Libraries**: HuggingFace Transformers, Scikit-learn, Sastrawi (for Indonesian stemming)[cite: 398, 442].

### Access the Code
You can view the full implementation and experimental results here:
👉 [Colab Notebook Implementation](https://colab.research.google.com/drive/1QJkOnwxJ7aEVKkcIk6wToW9WhTjbcbTu?usp=sharing)

---

## 📝 Citation
If you use this work or dataset in your research, please cite our Scopus-indexed paper:

```bibtex
@inproceedings{kevin2024emotion,
  title={Emotion Detection in Indonesian Music Comments Using BERT, Traditional Machine Learning and Their Hybrid Model},
  author={Kevin and Louis, Edrick and Maximillian, David Malcom and Purwandari, Kartika},
  year={2024},
  publisher={Bina Nusantara University}
}
