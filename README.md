# Parkinson’s Disease Detection Using Support Vector Machines (SVM)

## 1. Project Overview
This project focuses on the development of a predictive system designed to detect **Parkinson’s Disease (PD)** using voice measurements. By leveraging machine learning techniques, specifically **Support Vector Machines (SVM)**, the system analyzes various vocal features to classify individuals as either **healthy** or **Parkinson's positive**.

---

## 2. System Architecture
The system follows a standard machine learning pipeline:

**Data Acquisition → Pre-processing → Feature Scaling → Model Training → Evaluation**

---

## 2.1 Dataset Description
- **Source:** The dataset is loaded from a CSV file containing **195 instances**  
- **Dimensionality:** The dataset consists of **24 columns**, including:
  - 22 vocal features  
  - 1 unique identifier (`name`)  
  - 1 target label (`status`)  

### Key Features
- **Fundamental Frequency**
  - MDVP:Fo(Hz)  
  - MDVP:Fhi(Hz)  
  - MDVP:Flo(Hz)  

- **Jitter and Shimmer**
  - Measures variation in fundamental frequency and amplitude  

- **Noise Measures**
  - NHR (Noise-to-Harmonics Ratio)  
  - HNR (Harmonics-to-Noise Ratio)  

### Target Variable (status)
- `0` → Healthy  
- `1` → Parkinson's Positive  

---

## 2.2 Data Pre-processing
- **Handling Null Values:**  
  An initial check confirmed that the dataset contains **no missing values**  

- **Feature Separation:**  
  - Dropped `name` and `status` columns to isolate feature set (X)  
  - Target variable stored as (Y)  

- **Standardization:**  
  Since vocal features vary significantly in scale, a **StandardScaler** is applied to normalize the data.  
  This ensures that the SVM model treats all features with equal importance.

---

## 3. Model Implementation
The system utilizes a **Support Vector Machine (SVM)** with a **linear kernel**.

### Why SVM?
SVM is highly efficient in high-dimensional spaces, making it ideal for medical datasets with numerous features but limited samples.

### Training Details
- **Train-Test Split:**  
  - 80% Training Data  
  - 20% Testing Data  

- **Training Process:**
```python
model.fit(X_train, Y_train)
