## ML-Powered Intrusion Detection System (IDS)

## Project Overview

This project implements a Machine Learning-based Intrusion Detection System (IDS) to monitor network traffic and classify connections as either **Normal** or various types of **Attack**. It demonstrates a practical application of data science techniques in a critical cybersecurity context.

The goal was to build a robust, high-accuracy classifier capable of detecting known and novel network threats, reducing false positives, and providing actionable security insights.


## Key Results & Performance

The model was rigorously tested on a held-out validation set. The performance metrics below showcase its efficacy in a high-stakes security environment

This IDS model was trained and evaluated using the NSL-KDD dataset, which contains various categorized network flow records.

The data preprocessing involved:
* Handling imbalanced classes (crucial for IDS).
* One-Hot Encoding of categorical features (e.g., protocol type, flag).
* Feature Scaling (Normalization/Standardization).

