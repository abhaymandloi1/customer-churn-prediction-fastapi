# customer_churn_prediction

## 📌 Project Overview

This project focuses on predicting customer churn using Machine Learning techniques. The core model is trained in a Jupyter Notebook using **XGBoost**, and the trained model is deployed using **two different approaches**:

1. **FastAPI** – for API-based predictions with interactive Swagger UI
2. **Flask** – for a simple web-based interface using HTML templates

The goal of the project is to demonstrate an **end-to-end ML workflow**: data analysis, model training, serialization, and deployment.

---

## 🧠 Problem Statement

Customer churn is a critical problem for subscription-based businesses. Predicting whether a customer is likely to leave helps companies take proactive retention measures.

This project predicts whether a telecom customer will churn based on historical customer data.

---

## 📊 Dataset

* **Name:** Telco Customer Churn Dataset
* **Source:** kaggle (public dataset)
* **File:** `WA_Fn-UseC_-Telco-Customer-Churn.csv`

The dataset includes customer demographics, account information, services used, and churn labels.

---

## ⚙️ Model Development (Jupyter Notebook)

* Performed data cleaning and preprocessing
* Encoded categorical features using label encoding
* Scaled numerical features
* Trained an **XGBoost Classifier**
* Evaluated model performance
* Saved trained artifacts using `pickle`

Files generated:

* `best_model.pkl`
* `encoder.pkl`
* `scaler.pkl`

---

## 🚀 Deployment Approaches

### 1️⃣ FastAPI Deployment (API + Swagger UI)

* Built a REST API using **FastAPI**
* Interactive API documentation available via Swagger UI
* Accepts customer details as input and returns churn prediction

Main file:

* `fastapi_app.py`

---

### 2️⃣ Flask Deployment (Web Interface)

* Built a web application using **Flask**
* HTML frontend for user-friendly input
* Displays churn prediction result on the web page

Main components:

* `app.py`
* `templates/index.html`
* `static/` (CSS/images)

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* FastAPI
* Flask
* HTML/CSS

---

## 📁 Project Structure

```
customer-churn-prediction-fastapi/
│
├── app.py                 # Flask application
├── fastapi_app.py         # FastAPI application
├── Customer Churn Prediction.ipynb  # Model training notebook
├── best_model.pkl         # Trained XGBoost model
├── encoder.pkl            # Feature encoder
├── scaler.pkl             # Feature scaler
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── templates/
│   └── index.html
├── static/
│   └── images / assets
├── README.md
└── .gitignore
```

---

## ▶️ How to Run

### Run FastAPI

```bash
uvicorn fastapi_app:app --reload
```

Then open:

```
http://127.0.0.1:8000/docs
```

### Run Flask App

```bash
python app.py
```

Then open:

```
http://127.0.0.1:5000
```

---

## ✅ Key Learnings

* End-to-end ML project workflow
* Model deployment using both API-based and UI-based approaches
* Practical experience with FastAPI, Flask, and Swagger

---

## 📌 Future Improvements

* Add Docker support
* Improve UI styling
* Add authentication and logging
* Deploy on cloud platform (Render / AWS / GCP)

---

## 👤 Author

**Abhay**

---

⭐ If you find this project useful, feel free to star the repository!
