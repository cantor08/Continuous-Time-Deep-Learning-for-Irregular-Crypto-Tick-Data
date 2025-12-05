# 📘 Modeling Irregular Financial Tick Data with Continuous Recurrent Units (CRU)
### *A Comparative Study with GRU on High-Frequency Cryptocurrency Markets*

---

### **Author Information**
**Name:** Maulik Sanjaykumar Raval  
**Student ID:** 200531711  
**Email:** mrr373@uregina.ca  
**Subject:** CS715 – Advanced Data Science & Machine Learning  
**Department:** Computer Science  
**University:** University of Regina  
**Location:** Regina, Canada  

---
## 🔍 Project Overview

This project explores how Continuous Recurrent Units (CRU) model irregularly sampled high-frequency financial tick data and compares their performance against a standard Gated Recurrent Unit (GRU). Using over 200,000 BTCUSDT perpetual futures trades, the study builds a complete preprocessing pipeline, incorporates time-gap (∆t) features, and evaluates GRU vs. CRU for short-term price direction forecasting. The goal is to understand whether continuous-time models offer measurable improvements when working with real-world, unevenly spaced market data.

## 📂 Repository Structure

- **CS715_PROJECT.ipynb** — Main Google Colab notebook (modeling + evaluation)
- **Project_Report.pdf** — Complete academic project report
- **README.md** — GitHub documentation for the project


## 🧠 Key Concepts

### **1. Irregular Time Series**
Financial tick data is recorded at uneven time intervals. Traditional RNNs assume fixed sampling, making them less effective for real-world market dynamics.

### **2. Continuous Recurrent Units (CRU)**
CRUs allow hidden states to evolve in continuous time using decay dynamics. They naturally incorporate time gaps (∆t) and better capture irregular patterns.

### **3. Gated Recurrent Unit (GRU) Baseline**
GRUs operate in discrete, fixed time steps. While effective for many tasks, they cannot fully leverage irregular time intervals present in financial data.

### **4. High-Frequency Cryptocurrency Markets**
BTCUSDT futures trades arrive rapidly and irregularly. Modeling these sequences requires architectures that understand temporal gaps and event-driven behavior.

## ⚙️ Methodology

### **1. Data Preprocessing**
- Loaded BTCUSDT perpetual futures dataset (200,000+ trades)
- Computed inter-trade time gaps (∆t) to capture irregularity
- Normalized numerical features for stable training
- Created sequences of 50 consecutive trades for supervised learning

### **2. Model Training**
- Implemented two models:
  - **GRU** — standard discrete-time recurrent baseline
  - **CRU** — continuous-time recurrent architecture with decay dynamics
- Both models trained using:
  - Binary cross-entropy loss
  - Adam optimizer
  - Chronological train/validation/test split

### **3. Evaluation Metrics**
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- AUC  
- Brier Score  
- McNemar Test for statistical significance

This pipeline ensures a fair and meaningful comparison between GRU and CRU in an irregular time-series environment.

## 📊 Results Summary

The experiment compares CRU and GRU on high-frequency BTCUSDT tick data to evaluate their ability to model irregular time intervals.

| Model | Accuracy | F1 Score | AUC | Notes |
|-------|----------|----------|------|------|
| **GRU** | ~0.520 | ~0.383 | ~0.523 | Serves as the discrete-time baseline |
| **CRU** | **~0.524** | **~0.437** | **~0.532** | Better handling of irregular ∆t improves performance |

### **Key Findings**
- CRU outperforms GRU in **all major metrics**.
- Continuous-time decay dynamics help model irregular gaps more effectively.
- McNemar Test indicates **statistically meaningful difference** (CRU > GRU).
- Improvements are modest but consistent — expected in noisy high-frequency markets.

**Conclusion:**  
CRU demonstrates a **clear modeling advantage** in irregular financial time-series forecasting.
