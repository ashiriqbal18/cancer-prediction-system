# cancer-prediction-system

## 📌 Project Overview

This project is an **AI-powered medical assistant** developed as a **semester project for the course *Programming for Artificial Intelligence***.
The system uses **machine learning models** to predict multiple cancer-related outcomes based on patient lifestyle, environmental, and genetic risk factors.

⚠️ **Disclaimer:**
This project is intended **only for academic and research purposes**. It is **not a medical diagnostic tool** and should not be used for real clinical decisions.


## 🎯 Objectives

The main goals of this project are:

* To apply **machine learning techniques** to healthcare-related data
* To build an **end-to-end AI pipeline**, from data analysis to deployment
* To create an **interactive web-based interface** for model predictions
* To demonstrate practical understanding of **classification and regression problems**


## 🔍 Features

The system predicts the following outcomes:

* 🧫 **Cancer Type** (Classification)
* 📌 **Cancer Stage** (Classification)
* ⚠️ **Severity Score** (Regression)
* 💰 **Estimated Treatment Cost**
* ⏳ **Estimated Survival Years**

### 🧑‍⚕️ Input Features

* Age
* Gender
* Country / Region
* Genetic Risk
* Air Pollution Exposure
* Alcohol Use
* Smoking Level
* Obesity Level


## 📊 Dataset Description

* **Dataset Size:** 50,000 patient records
* **Time Period:** 2015 – 2024
* **Source:** Synthetic global cancer patient dataset (academic use)

### 📁 Key Columns

* Demographic data (Age, Gender, Country)
* Risk factors (Genetic Risk, Pollution, Smoking, Alcohol, Obesity)
* Medical outcomes (Cancer Type, Stage, Severity Score)
* Financial and survival metrics

✔ No missing values
✔ No duplicate records


## 📈 Exploratory Data Analysis (EDA)

EDA was performed to understand data distribution and relationships:

* Distribution plots and boxplots for numerical features
* Correlation analysis with target variables
* Analysis of cancer severity across:

  * Cancer stages
  * Gender
  * Country / Region
  * Cancer types

### 🔗 Key Insights

* Smoking, genetic risk, and air pollution show strong correlation with severity
* Treatment cost and survival years show weak correlation with input features
* Cancer severity varies across stages and cancer types


## 🧠 Machine Learning Models

### 🧪 Model Types Used

| Task                      | Model                    |
| ------------------------- | ------------------------ |
| Cancer Type Prediction    | Random Forest Classifier |
| Cancer Stage Prediction   | Random Forest Classifier |
| Severity Score Prediction | Random Forest Regressor  |
| Treatment Cost Prediction | Random Forest Regressor  |
| Survival Years Prediction | Random Forest Regressor  |


### ⚙️ Preprocessing Pipeline

* Numerical Features → StandardScaler
* Categorical Features → OneHotEncoder
* Combined using `ColumnTransformer`
* Models wrapped using `Pipeline` for clean deployment


## 📊 Model Performance

### 🔹 Classification Models

* **Cancer Type Accuracy:** ~13%
* **Cancer Stage Accuracy:** ~20%

> *Note:* Low accuracy is expected due to overlapping feature distributions and limited predictive medical indicators.

### 🔹 Regression Models

* **Severity Score:**

  * MAE ≈ 0.49
  * R² ≈ 0.77

* **Treatment Cost & Survival Years:**

  * Low R² due to weak correlation with input features


## 🖥️ Web Application (Streamlit)

An interactive **Streamlit web application** was developed to allow users to:

* Enter patient information via sliders and dropdowns
* Generate predictions instantly
* View results in a clean and user-friendly layout

### 🧩 App Pages

* Home Page (Project overview)
* Prediction Page (User inputs & outputs)


## 🚀 Deployment

* Application deployed using **Streamlit**
* Public access enabled via **ngrok**
* Models serialized using `joblib`


## 📂 Project Structure


├── app.py
├── model_type_no_year.pkl
├── model_stage_no_year.pkl
├── model_severity_no_year.pkl
├── model_cost_no_year.pkl
├── model_survival_no_year.pkl
├── global_cancer_patients_2015_2024.csv
├── README.md



## 🛠️ Technologies Used

* **Programming Language:** Python
* **Libraries:**

  * Pandas, NumPy
  * Scikit-learn
  * Matplotlib, Seaborn
  * Streamlit
  * Joblib


## ▶️ How to Run the Project

### 1️⃣ Install dependencies

pip install pandas numpy scikit-learn streamlit joblib matplotlib seaborn


### 2️⃣ Run the app

streamlit run app.py
