---

### Diabetes Classification ML Project

Predict diabetes using Machine Learning with a clean pipeline, hyperparameter tuning, and full evaluation.

### Overview

This project builds a multi-class classifier to predict:
**N (Non-Diabetic), P (Pre-Diabetic), Y (Diabetic)** using real medical data.
Includes preprocessing, exploratory data analysis (EDA), model training, tuning, and performance evaluation.

### Key Features

* Clean and structured dataset
* Medical feature analysis
* Models: Decision Tree, SVM, KNN
* Scaling, encoding, and hyperparameter tuning
* Visualization and evaluation reports

### Dataset

* ~1000 patient records
* 14 medical features
* Target classes → N / P / Y
* Features include Age, BMI, HbA1c, LDL, HDL, Urea, Creatinine

### Preprocessing

* Unified & cleaned CLASS labels
* Encoded Gender & Class
* Removed ID columns
* Applied StandardScaler
* Stratified train/validation/test split

### Models and Performance

| Model         | Accuracy | F1-Score | Remarks                 |
| ------------- | -------- | -------- | ----------------------- |
| Decision Tree | 99%      | 0.9898   | Best performing model   |
| SVM           | 96%      | 0.9604   | Strong alternative      |
| KNN           | 94%      | 0.9353   | Good but slightly noisy |

**Decision Tree** is the top model for this dataset.

### Model Details

* **Decision Tree**: Tuned `max_depth`, `min_samples_split`
* **SVM**: RBF kernel, tuned `C`, `gamma`
* **KNN**: Tuned `k` and distance metrics

### Run the Project

```bash
git clone https://github.com/jawzalanazi/Diabetes-Prediction.git
cd Diabetes-Prediction
jupyter notebook
```

### Project Structure

```
diabetes-ml-project/
│── ML_Project.ipynb
│── diabetes.csv
│── README.md
└── results/
      ├── tree_confusion.png
      ├── svm_confusion.png
      └── knn_confusion.png
```

### Authors

* Jawza Al-Anazi
* Danah Al-Ghezii
* Ghaida Al-Dowsary
* Nazek Al-Zaid

---
