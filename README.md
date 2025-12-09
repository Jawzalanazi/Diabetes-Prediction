# Diabetes Classification using Machine Learning

This project aims to predict a patient's diabetes status — **Non-Diabetic (N), Pre-Diabetic (P), or Diabetic (Y)** — using machine learning models trained on real medical data.  
Three algorithms were implemented and compared: **Decision Tree, SVM, and KNN**.

---

## 📌 Project Objectives
- Clean and preprocess real hospital diabetes data.
- Explore feature correlations and class imbalance.
- Train and tune ML models (Decision Tree, SVM, KNN).
- Evaluate the models using Accuracy, F1-Score, and Confusion Matrices.
- Identify the most reliable model for multiclass diabetes prediction.

---

## 📊 Dataset Overview
- **~1000 records**, **14 medical features**
- Key variables include: Age, Gender, BMI, Urea, Creatinine, HbA1c, Cholesterol, LDL, HDL, TG, VLDL.
- **Target classes:**  
  - `Y` → Diabetic  
  - `N` → Non-Diabetic  
  - `P` → Pre-Diabetic
- Majority class: **Y**, Minority class: **P**

---

## 🧼 Data Preprocessing
- Standardized CLASS labels (Y/N/P)
- Encoded categorical variables using **LabelEncoder**
- Dropped ID-like columns (No_Pation / ID)
- Applied **StandardScaler** for SVM and KNN
- Stratified Train/Validation/Test split:
  - 64% Train
  - 16% Validation
  - 20% Test

---

## 🔍 Exploratory Data Analysis (EDA)
- Class distribution visualization  
- Correlation heatmap of medical features  
- Identified strong indicators such as **HbA1c**, **BMI**, and **Urea**

---

## 🤖 Machine Learning Models

### **1️⃣ Decision Tree**
- Tuned with GridSearchCV (max_depth, min_samples_split, min_samples_leaf, criterion)
- **Best Performance**
- Captures threshold-based medical patterns (especially HbA1c)

### **2️⃣ Support Vector Machine (SVM)**
- Tuned C, gamma, and kernel (linear, poly, rbf)
- Effective at modeling non-linear relationships
- Slight difficulty distinguishing Pre-Diabetic class

### **3️⃣ K-Nearest Neighbors (KNN)**
- Tuned k, distance metrics, and weights
- Works well with scaled data
- Higher false positives for Non-Diabetic class

---

## 📝 Evaluation Metrics
Models were evaluated using:
- **Accuracy**
- **Weighted F1-Score**
- **Confusion Matrix**
- **Classification Report**

---

## ⭐ Results Summary (Test Set)

| Model           | Accuracy | F1-Score (Weighted) | Key Notes |
|-----------------|----------|----------------------|-----------|
| **Decision Tree** | **99%** | **0.9898** | Best model; excellent threshold detection |
| **SVM**          | 96%      | 0.9604               | Strong generalization; minor errors in P class |
| **KNN**          | 94%      | 0.9353               | Struggles with Non-Diabetic class |

**🏆 Best Model: Decision Tree**

---

## 🛠️ Technologies Used
- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  
- Scikit-Learn  
- Joblib  
- Google Colab  

---

## 🚀 How to Run the Project

### 1. Clone the repository
```bash
git clone https://github.com/jawzalanazi/Diabetes-Prediction.git
```
### 2. Install dependencies
pip install -r requirements.txt

### 3. Run the notebook
jupyter notebook


Or open it in Google Colab.

📦 Project Structure
📁 diabetes-ml-project
│── 📄 ML_Project.ipynb
│── 📄 diabetes.csv
│── 📄 README.md
└── 📁 results
      ├── confusion_matrix_svm.png
      ├── confusion_matrix_tree.png
      └── confusion_matrix_knn.png

      
## 👥 Authors
- **Jawza Fahad Al-Anazi**
- **Danah Sebhan Al-Ghezii**
- **Ghaida Saeed Al-Dowsary**
- **Nazek Turki Al-Zaid**


⭐ If you found this work useful, please star the repository!
