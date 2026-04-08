# Parkinson’s Disease Detection Using Support Vector Machines (SVM)

## 📌 Project Overview
This project develops a machine learning model to detect **Parkinson’s Disease (PD)** using voice measurement data.  
A **Support Vector Machine (SVM)** model is used to classify individuals as either healthy or Parkinson’s positive based on extracted vocal features.

---

## ⚙️ System Workflow
The system follows a standard machine learning pipeline:

Data Acquisition → Data Pre-processing → Feature Scaling → Model Training → Evaluation

---

## 📊 Dataset Information
- **Instances:** 195
- **Features:** 24 columns
  - 22 vocal features
  - 1 identifier (`name`)
  - 1 target (`status`)

### 🔑 Key Features
- **Fundamental Frequency**
  - MDVP:Fo(Hz), MDVP:Fhi(Hz), MDVP:Flo(Hz)
- **Jitter & Shimmer**
  - Measures variation in frequency and amplitude
- **Noise Measures**
  - NHR (Noise-to-Harmonics Ratio)
  - HNR (Harmonics-to-Noise Ratio)

### 🎯 Target Variable
- `0` → Healthy  
- `1` → Parkinson’s Positive  

---

## 🧹 Data Pre-processing
- No missing values found in the dataset  
- Dropped `name` and `status` columns to form feature set (X)  
- Target variable stored in (Y)  
- Applied **StandardScaler** for feature normalization  

---

## 🤖 Model Implementation
- **Algorithm:** Support Vector Machine (SVM)  
- **Kernel:** Linear  

### 🔀 Train-Test Split
- 80% Training Data  
- 20% Testing Data  

### 🏋️ Training
The model is trained using the processed and scaled dataset.

---

## 📈 Model Performance

| Metric | Score |
|--------|------|
| Training Accuracy | 88.46% |
| Test Accuracy | 87.18% |

✔ The model shows good generalization with minimal overfitting.

---

## 🔍 Prediction System

### ⚠️ Error Faced
- NameError: scaler not defined  

### 🛠️ Resolution
- Ensure the StandardScaler is properly initialized and fitted before making predictions  

### 🔄 Prediction Process
1. Convert input data into the required format  
2. Reshape data for single prediction  
3. Apply feature scaling  
4. Predict whether the person is healthy or Parkinson’s positive  

---

## 🚀 Technologies Used
- Python  
- NumPy  
- Pandas  
- Scikit-learn  

---

## ▶️ How to Run
1. Clone the repository  
2. Install required dependencies  
3. Run the main program  

---

## ✅ Conclusion
This project successfully demonstrates the use of **Support Vector Machines (SVM)** for detecting Parkinson’s Disease using vocal features.

The model achieves **high accuracy (88.46% training and 87.18% testing)**, indicating strong performance and good generalization. It highlights the potential of machine learning in assisting early diagnosis of Parkinson’s Disease.

Future improvements may include:
- Using **non-linear kernels (RBF)**  
- Applying **deep learning techniques**  
- Improving early-stage detection accuracy  

---

## 📄 License
This project is open-source and available under the MIT License.
