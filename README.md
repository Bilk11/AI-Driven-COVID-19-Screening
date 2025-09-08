# AI-Driven COVID-19 Screening for Hospitals

**A machine learning pipeline to predict COVID-19 status using patient data, optimizing hospital resource allocation and reducing unnecessary testing.**

---

## **📌 Overview**
This project develops a **Random Forest Classifier** to predict COVID-19 status based on patient symptoms, vital signs, and demographic data. The goal is to help hospitals:
- **Prioritize high-risk patients** for testing and isolation.
- **Reduce unnecessary tests** by 20% (improving precision).
- **Achieve ≥95% recall** for positive cases (minimizing missed diagnoses).

---

## **📊 Data**
### **Sources**
- Two hospital datasets (`hospital1.csv`, `hospital2.csv`) with:
  - **54 columns**: Symptoms, vitals, demographics, and PCR results.
  - **27,446 records** after merging and cleaning.

### **Key Features**
| Feature                | Description                          |
|------------------------|--------------------------------------|
| `fever_temperature`    | Body temperature (°C)                |
| `oxygen_saturation`    | Blood oxygen level (%)               |
| `history_of_fever`     | Binary (0/1)                         |
| `cough`                | Binary (0/1)                         |
| `age`                  | Patient age                          |
| `PCR_result`           | Target: 0 (negative), 1 (positive)   |

### **Preprocessing**
- **Handled missing values**: Mean/median imputation.
- **Outlier correction**: Replaced invalid oxygen saturation values.
- **Standardization**: Aligned column names and data types.
- **Categorical encoding**: One-hot encoding for non-numeric features.

---

## **🛠️ Model**
### **Random Forest Classifier**
- **Performance Metrics**:
  | Metric       | Score  |
  |--------------|--------|
  | Accuracy     | 85%    |
  | Precision    | 86%    |
  | Recall       | 99%    |
  | F1-Score     | 92%    |

- **Feature Importance**:
  ![Top Features](https://via.placeholder.com/400x200?text=Top+Features:+Age,+Fever,+Oxygen+Saturation,+Fatigue)
  *(Age, fever temperature, and oxygen saturation were top predictors.)*

### **Decision Tree**
- **Interpretable splits** (e.g., cough, fever, vomiting).
- **Visualization**:
  ![Decision Tree](https://via.placeholder.com/400x200?text=Decision+Tree+Visualization)

---

## **📈 Results**
- **ROC Curve**:
  ![ROC Curve](https://via.placeholder.com/400x200?text=ROC+Curve+AUC%3D0.95)
  *(AUC = 0.95, indicating strong discriminatory power.)*
- **Business Impact**:
  - **Reduced testing burden** by filtering low-risk patients.
  - **Improved bed allocation** with early identification of positive cases.

---

## **🔧 Setup**
### **Requirements**
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### **Run the Pipeline**
1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/covid19-screening.git
   ```
2. Navigate to the project:
   ```bash
   cd covid19-screening
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook 2nd_Assignment_Data_Processes.ipynb
   ```

---

## **📂 Repository Structure**
```
covid19-screening/
├── data/
│   ├── hospital1.csv          # Raw dataset 1
│   └── hospital2.csv          # Raw dataset 2
├── notebooks/
│   └── 2nd_Assignment_Data_Processes.ipynb  # Analysis & modeling
├── README.md                   # This file
└── requirements.txt            # Dependencies
```

---

## **🚀 Future Work**
- **Deploy as a web app** for real-time hospital use.
- **Test on new datasets** for generalizability.
- **Optimize feature engineering** for higher precision.

---

## **📜 License**
This project is licensed under the **MIT License**.

---
