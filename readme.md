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
│   ├── attention_maps/
│   ├── shap_outputs/
│   └── lime_outputs/
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
jupyter notebook transformer_kaggle.ipynb
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

The Transformer model achieved good sentiment classification performance and provided explainable predictions using attention visualization, SHAP, and LIME.

---

# requirements.txt

transformers
torch
numpy
pandas
matplotlib
seaborn
scikit-learn
datasets
shap
lime
jupyter

