# 💳 Credit Card Fraud Detection Model

A machine learning project that detects **fraudulent credit card transactions** using behavioral and transactional features.

The model predicts whether a transaction is **fraudulent or legitimate** and assigns a **risk score** to help financial institutions detect suspicious activity.

---

## 📌 Problem Statement

Credit card fraud causes billions of dollars in financial losses every year.
Traditional rule-based systems often fail to detect new fraud patterns.

This project builds a **machine learning fraud detection model** that analyzes transaction behavior and flags suspicious transactions in real time.

---

## 📊 Dataset Features

The dataset contains transaction-level features such as:

* `amount`
* `transaction_hour`
* `merchant_category`
* `foreign_transaction`
* `location_mismatch`
* `device_trust_score`
* `velocity_last_24h`
* `cardholder_age`

Target variable:

* `is_fraud`
  (1 = Fraudulent transaction, 0 = Legitimate transaction)

---

## ⚠️ Machine Learning Challenge

Fraud detection is a **highly imbalanced classification problem**:

* Legitimate transactions dominate the dataset
* Fraud cases are rare but critical

Because of this, **accuracy alone is not a good metric**.

The model is optimized for:

* **High recall** → detect as many fraud cases as possible
* **Reasonable precision** → avoid too many false alerts

---

## 🧠 Model Used

**XGBoost Classifier**

Why XGBoost?

* Handles class imbalance well
* Strong performance on tabular data
* Captures nonlinear fraud patterns

---

## 📈 Model Performance

| Metric    | Score |
| --------- | ----- |
| Precision | ~25%  |
| Recall    | ~93%  |
| F1 Score  | ~39%  |

High recall ensures most fraudulent transactions are detected.

---

## 🧠 Risk Scoring

Instead of only predicting fraud/non-fraud, the model also outputs a **fraud probability score**.

This allows financial systems to:

* rank transactions by risk
* investigate only high-risk transactions
* reduce manual review workload

---

## 🗂 Project Structure

```text
 FRAUD_DETECTION/
│
├── data/
│   └── credit_card_fraud_10k.csv
│
├── model/
│   └── fraud_detection_model.pkl
│
├── notebooks/
│   └── gradient_boosting.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ⚙️ Machine Learning Workflow

1. **Data Preprocessing**

   * Handling categorical features
   * Encoding merchant categories

2. **Feature Engineering**

   * Transaction velocity features
   * Device trust indicators
   * Location mismatch signals

3. **Model Training**

   * XGBoost classifier
   * Handling class imbalance

4. **Evaluation**

   * Precision
   * Recall
   * F1 Score
   * Confusion matrix

---

## 🚀 How to Run

### Clone the repository

### Install dependencies

```bash
pip install -r requirements.txt
```

### Train the model

### Generate fraud risk scores

## 🔮 Future Improvements

* Implement **real-time fraud detection API**
* Deploy model using **FastAPI**
* Add **SHAP explainability**
* Build fraud monitoring dashboard

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost

---
"# credit-fraud-detector" 
