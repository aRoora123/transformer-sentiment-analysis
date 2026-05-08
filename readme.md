# README.md

# Transformer Sentiment Analysis with Attention, SHAP, and LIME

This project performs sentiment classification using a Transformer-based NLP model on the Amazon Polarity dataset. The project also analyzes Transformer attention layers and explains predictions using SHAP and LIME.

---

# Features

- Transformer fine-tuning using Hugging Face
- Attention layer visualization
- SHAP explanations
- LIME explanations
- Runtime comparison
- Error analysis

---

# Dataset

Dataset used:

https://huggingface.co/datasets/fancyzhx/amazon_polarity

A subset of the dataset was used because the project was trained on Kaggle.

---

# Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- SHAP
- LIME
- Scikit-learn
- Matplotlib
- Seaborn
- Kaggle Notebook Environment

---

# Hardware and Software

Hardware:
- Kaggle GPU: Tesla T4
- RAM: 16 GB

Software:
- Python 3.12
- PyTorch
- Transformers
- SHAP
- LIME
- Jupyter Notebook / Kaggle Notebook

---

# Project Structure

project/
│
├── transformer_kaggle.ipynb
├── README.md
├── requirements.txt
├── outputs/
|   |──distilbert_evaluation_matrix/
│   ├── attention_maps/
│   ├── shap_outputs/
│   ├── lime_outputs/
│   ├── error-analysis_runtime-comparision/
│   └── shap_vs_lime/
└── report.pdf

---

# Installation

Install required libraries:

```bash
pip install -r requirements.txt
```

---

# Running the Project

Open the Kaggle notebook and run all cells step by step.

If running locally:

```bash
transformer-sentiment-analysis-project-urwatehseen.ipynb
```

---

# Workflow

1. Load Dataset
2. Clean and Tokenize Data
3. Fine-tune Transformer Model
4. Evaluate Performance
5. Analyze Attention Maps
6. Generate SHAP Explanations
7. Generate LIME Explanations
8. Compare SHAP and LIME
9. Perform Error Analysis

---
# Results

The fine-tuned DistilBERT model achieved **93% accuracy** on a balanced 1,000-sample IMDb test set, with 0.93 precision, recall, and F1-score across both positive and negative classes — indicating no bias toward either sentiment.

| Class        | Precision | Recall | F1-Score |
|--------------|-----------|--------|----------|
| Negative     | 0.93      | 0.92   | 0.92     |
| Positive     | 0.93      | 0.93   | 0.93     |
| **Weighted Avg** | **0.93** | **0.93** | **0.93** |

### Explainability
- **Attention Analysis** — Final-layer [CLS] token attention confirmed the model focuses on sentiment-bearing words (e.g., *terrible*, *outstanding*) rather than stopwords.
- **SHAP** — Identified globally influential tokens such as *good*, *great*, and *boring*, with high faithfulness and stability (~28s/sample).
- **LIME** — Provided fast local explanations (~8.4s/sample) highlighting key drivers per prediction, useful for quick debugging.

### Error Analysis
The 73 misclassified samples were primarily caused by **sarcasm**, **negation constructs**, and **mixed-sentiment** reviews — known limitations of token-level models.


