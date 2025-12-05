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

.
├── CS715_PROJECT.ipynb        # Main Google Colab notebook (modeling + evaluation)
├── CS715_Report.pdf           # Full academic project report
├── README.md                  # Documentation for GitHub repo
└── data/                      # (Optional) dataset folder if downloaded locally

## 🧠 Key Concepts

### **1. Irregular Time Series**
Financial tick data is recorded at uneven time intervals. Traditional RNNs assume fixed sampling, making them less effective for real-world market dynamics.

### **2. Continuous Recurrent Units (CRU)**
CRUs allow hidden states to evolve in continuous time using decay dynamics. They naturally incorporate time gaps (∆t) and better capture irregular patterns.

### **3. Gated Recurrent Unit (GRU) Baseline**
GRUs operate in discrete, fixed time steps. While effective for many tasks, they cannot fully leverage irregular time intervals present in financial data.

### **4. High-Frequency Cryptocurrency Markets**
BTCUSDT futures trades arrive rapidly and irregularly. Modeling these sequences requires architectures that understand temporal gaps and event-driven behavior.
