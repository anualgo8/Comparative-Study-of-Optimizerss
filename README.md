

---

# 🛍️ E-COMMERCE TEXT CLASSIFICATION USING MULTIPLE OPTIMIZERS

### 📘 Project Overview

This project implements an **E-commerce product text classification system** using deep learning techniques.
The model classifies product descriptions into appropriate **categories** such as *Household, Clothing, Electronics,* etc.
It also compares the performance of multiple **optimizers** — including **SGD, Adam, RMSProp, Adagrad, and Nadam** — to determine which provides the best accuracy and convergence speed.

---

## 🧭 Workflow

Each step is modular and automated — from dataset loading to model evaluation.

```
Dataset → Preprocessing → Tokenization → Model Training (with multiple optimizers) → Evaluation → Visualization
```

---

## ⚙️ Features

✅ Automatic dataset download from Kaggle via `kagglehub`
✅ Tokenization and padding using TensorFlow’s `Tokenizer`
✅ Multi-class label encoding for product categories
✅ Training and validation with five optimizers (SGD, Adam, RMSProp, Adagrad, Nadam)
✅ Comparative analysis of accuracy and loss curves
✅ Reproducibility through fixed random seeds

---

## 📂 Input Dataset

**Source:** [Kaggle — E-commerce Text Classification Dataset](https://www.kaggle.com/datasets/saurabhshahane/ecommerce-text-classification)

**Sample Columns:**

| Column   | Example                                                   |
| -------- | --------------------------------------------------------- |
| Category | Household                                                 |
| Text     | SAF 'Floral' Framed Painting (Wood, 30 inch x 40 inch)... |

> The dataset contains product descriptions and their associated categories, enabling text-based classification using deep learning.

---

## 🧠 How It Works

### 1️⃣ Dataset Loading

The dataset is automatically fetched using:

```python
import kagglehub
path = kagglehub.dataset_download("saurabhshahane/ecommerce-text-classification")
```

### 2️⃣ File Detection

Identifies the main `.csv` file dynamically and loads it as a DataFrame.

### 3️⃣ Data Preparation

* Extracts **text** and **label** columns.
* Encodes labels numerically.
* Splits dataset into **train** and **test** sets using `train_test_split`.

### 4️⃣ Tokenization & Padding

Converts text into sequences and pads all samples to the same length for uniformity.

### 5️⃣ Model Training

Each optimizer (SGD, Adam, RMSProp, Adagrad, Nadam) trains the same neural network architecture to compare accuracy and convergence speed.

### 6️⃣ Evaluation

Plots accuracy and loss graphs for all optimizers and summarizes their final validation metrics.

---

## 📊 Example Results

| Optimizer | Final Validation Accuracy | Final Validation Loss |
| --------- | ------------------------- | --------------------- |
| Adam      | 0.89                      | 0.31                  |
| RMSProp   | 0.87                      | 0.35                  |
| Nadam     | 0.88                      | 0.34                  |
| Adagrad   | 0.72                      | 0.68                  |
| SGD       | 0.65                      | 0.75                  |

✅ **Adam**, **Nadam**, and **RMSProp** achieve the best results, while **SGD** and **Adagrad** show slower learning and higher loss values.

---

## 🚀 How to Run the Script

### 🧱 Prerequisites

* **Python 3.8+**
* Install dependencies:

  ```bash
  pip install tensorflow pandas scikit-learn kagglehub matplotlib
  ```

### ▶️ Run the Notebook

Execute all cells sequentially:

```
1. Dataset download  
2. Data preprocessing  
3. Tokenization & encoding  
4. Model training with multiple optimizers  
5. Evaluation & visualization  
```

---

## 📤 Outputs

* Accuracy and loss graphs for each optimizer
* Final summary table comparing all optimizers
* Sample predictions on test data

---

## 🤝 Contributors

* **Anushika Gupta** — Model Design & Optimizer Analysis
* **Akash saraswat** — Data Preparation
* **suryansh jain** — Evaluation Scripts

---

### 🧑‍🏫 Supervised by

* *Dr. Rajni Ranjan Singh* (HoD, CAI Department, MITS, Gwalior)

---

## 📜 License

This repository is provided for **academic and educational purposes** only.
Reproduction or redistribution without permission is prohibited.

---

## ⭐ Acknowledgment

We thank **Madhav Institute of Technology and Science (MITS), Gwalior**
for their guidance and support in completing this research project.

---

© 2025 — Team **E-COMMERCE TEXT CLASSIFICATION**
*All rights reserved.*

