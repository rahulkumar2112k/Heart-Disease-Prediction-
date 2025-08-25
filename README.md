# ❤️ Heart Disease Prediction using Machine Learning  

---

## 📌 Project Overview  

Heart disease is one of the leading causes of death worldwide. Early detection can save lives by enabling timely interventions.  
This project implements a **Machine Learning model** to predict whether a person is likely to have **Heart Disease** based on key medical attributes such as age, blood pressure, cholesterol, heart rate, and more.  

**Goal:** Provide a data-driven predictive system to assist healthcare professionals and patients in early risk detection.  

---

## ⚙️ Tech Stack & Libraries  

- **Python** 🐍  
- **Pandas & NumPy** → Data handling  
- **Matplotlib & Seaborn** → Data visualization  
- **Scikit-learn** → Machine Learning (Logistic Regression)  

---

## 📂 Dataset Information  

The dataset contains the following features:  

| Feature   | Description |
|-----------|-------------|
| age       | Age of the patient |
| sex       | Sex (0 = Female, 1 = Male) |
| cp        | Chest pain type (0-3) |
| trestbps  | Resting blood pressure |
| chol      | Serum cholesterol (mg/dl) |
| fbs       | Fasting blood sugar > 120 mg/dl (1 = True; 0 = False) |
| restecg   | Resting ECG results (0-2) |
| thalach   | Maximum heart rate achieved |
| exang     | Exercise induced angina (1 = Yes, 0 = No) |
| oldpeak   | ST depression induced by exercise |
| slope     | Slope of ST segment (0-2) |
| ca        | Number of major vessels (0-3) |
| thal      | Thalassemia (1 = Normal, 2 = Fixed defect, 3 = Reversible defect) |
| target    | Heart Disease (0 = No, 1 = Yes) |

---

## 📊 Data Analysis  

- Dataset contains both **categorical and numerical features**.  
- The target variable `Heart Disease` is balanced:  
  - 0 → No Heart Disease  
  - 1 → Heart Disease  
- Features were analyzed to identify strong correlations with the target variable.  

**Correlation Highlights:**  
- `thalach` (Max Heart Rate) → Strong negative correlation with heart disease  
- `oldpeak` (ST depression) → Strong positive correlation with heart disease  
- `cp` (Chest Pain type) → Significant positive correlation  

---

## 🤖 Model Training & Accuracy  

**Model Used:** Logistic Regression  

| Dataset      | Accuracy Score |
|-------------|----------------|
| Training Set | 85%            |
| Test Set     | 83%            |

✅ High accuracy indicates the model can reliably classify patients at risk.  

---

## 📈 Confusion Matrix  

The model's predictions on test data can be visualized in a **confusion matrix**:  

  <img width="677" height="567" alt="image" src="https://github.com/user-attachments/assets/4336db35-33a3-4a30-afde-6d91523d8f82" />

  |               | Predicted No | Predicted Yes |
|---------------|--------------|---------------|
| Actual No     | 23           | 5             |
| Actual Yes    | 6            | 27            |

- **True Negative (23):** Correctly predicted no heart disease  
- **True Positive (27):** Correctly predicted heart disease  
- **False Negative (6):** Missed predictions of heart disease  
- **False Positive (5):** Incorrectly predicted heart disease  


---

## 🖥️ Predictive System (Console-based)  

Users can input patient medical details and get **instant predictions**.  

### Example Input & Output  

```text
❤️ Heart Disease Prediction System ❤️
👤 Enter Age: 52
⚧ Enter Sex (0 = Female, 1 = Male): 1
💓 Enter Chest Pain Type (0-3): 0
🩸 Enter Resting Blood Pressure: 125
🥚 Enter Serum Cholesterol (mg/dl): 212
🍬 Fasting Blood Sugar > 120 mg/dl (1 = True, 0 = False): 0
📉 Resting ECG results (0-2): 1
🏃 Max Heart Rate Achieved: 168
😮 Exercise Induced Angina (1 = Yes, 0 = No): 0
📉 ST Depression induced by exercise: 1.0
📈 Slope of ST Segment (0-2): 2
🩺 Number of major vessels (0-3): 0
🧬 Thalassemia (1 = Normal, 2 = Fixed defect, 3 = Reversible defect): 2

✅ Prediction: The person is LIKELY to have Heart Disease.
