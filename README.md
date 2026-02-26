## ML-Powered Intrusion Detection System (IDS)

## Project Overview

This project implements a Machine Learning-based Intrusion Detection System (IDS) to monitor network traffic and classify connections as either **Normal** or various types of **Attack**. It demonstrates a practical application of data science techniques in a critical cybersecurity context.

The goal was to build a robust, high-accuracy classifier capable of detecting known and novel network threats, reducing false positives, and providing actionable security insights.


## Key Results & Performance

The model classifies network traffic as normal or malicious using the **Random Forest** algorithm on the **NSL-KDD** dataset. The model achieves **99% overall accuracy** across four major attack categories.

--

## 📋 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)

---

## 📌 Overview

Network intrusion detection is a critical component of modern cybersecurity. This project applies supervised machine learning to automatically detect and classify four types of network attacks:

| Attack Type | Description |
|---|---|
| **DoS** | Denial of Service — flooding a system to deny legitimate access |
| **Probe** | Surveillance attacks scanning for vulnerabilities |
| **R2L** | Remote-to-Local — unauthorized access from a remote machine |
| **U2R** | User-to-Root — privilege escalation attacks |

The model applies feature selection (13 optimal features) and cross-validation to ensure robust, generalizable performance.

---

## 📂 Dataset

**NSL-KDD** — an improved version of the KDD Cup 99 dataset, widely used as a benchmark for IDS research.

- Removes duplicate records present in KDD Cup 99
- Provides a balanced distribution across attack categories
- Split into training and test sets for fair evaluation

> Dataset source: [Canadian Institute for Cybersecurity](https://www.unb.ca/cic/datasets/nsl.html)

---

## ⚙️ Methodology

1. **Data Preprocessing** — handling missing values, encoding categorical features, normalization
2. **Feature Selection** — selected 13 most informative features using feature importance analysis
3. **Model Training** — Random Forest classifier trained with cross-validation
4. **Evaluation** — assessed using Accuracy, F1-Score, Precision, Recall, and Confusion Matrix

---

## 📊 Results

### Cross-Validation Performance (13 Selected Features)

| Attack Type | F-Score | Recall | Accuracy | Precision |
|---|---|---|---|---|
| **DoS** | 99.70% | 99.71% | 99.80% | 99.70% |
| **Probe** | 98.57% | 98.47% | 99.10% | 98.67% |
| **R2L** | 96.38% | 96.10% | 97.46% | 96.69% |
| **U2R** | 87.74% | 89.55% | 99.65% | 87.54% |
| **Average** | **95.60%** | **95.95%** | **99.00%** | **95.65%** |

### Key Highlights
- ✅ **99% overall accuracy** across all attack categories
- ✅ **99.80% accuracy** on DoS attacks — the most common attack type
- ✅ Low false positive rate on DoS (109 FP out of ~16,000 samples)
- ✅ Feature selection reduced dimensionality while maintaining high performance
