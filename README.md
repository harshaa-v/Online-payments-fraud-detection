Team ID – **LTVIP2026TMIDS62812**

Project – **Online Payments Fraud Detection using ML**

Team Members

1. **Geethika Nagaraju**
2. **Maddula Pavan Veerabhadra Srinaga Gopinadh**
3. **Manda Harsha Vardhan**
4. **Kotla Jithendra**

---

# 🛡️ Online Payments Fraud Detection using Machine Learning

A complete **Machine Learning + Flask web application** that detects fraudulent online payment transactions using multiple ML algorithms and deploys the selected model for real-time prediction.

---

## 🎯 Project Overview

This project builds a fraud detection system using historical online transaction data.
Multiple machine learning models were trained and compared, and the selected model was deployed using a Flask web application for real-time fraud detection.

After comparison, the **Support Vector Machine (SVC)** model was selected and deployed using a Flask web application for real-time fraud prediction.

---

## 🚀 Key Features

* Real-time fraud prediction using Flask
* Trained **5 ML models**:

  * Random Forest
  * Decision Tree
  * Extra Trees
  * Support Vector Machine (SVC)
  * XGBoost
* Model comparison using Accuracy & Cross Validation
* Stratified train-test split
* Class imbalance handling
* Model saved using Pickle
* Clean Flask-based UI (Home → Predict → Result)
* Final deployed model: **Support Vector Machine (SVC)**

---

## 📊 Dataset Features

**Dataset:** Online Payments Fraud Detection (Kaggle)

### Features Used

| Feature        | Description                         |
| -------------- | ----------------------------------- |
| step           | Time unit of transaction            |
| type           | Transaction type (Encoded 0–4)      |
| amount         | Transaction amount                  |
| oldbalanceOrg  | Sender balance before transaction   |
| newbalanceOrig | Sender balance after transaction    |
| oldbalanceDest | Receiver balance before transaction |
| newbalanceDest | Receiver balance after transaction  |
| isFraud        | Target (0 = Not Fraud, 1 = Fraud)   |

---

## 🧠 Machine Learning Models Trained

The following models were trained and evaluated:

* RandomForestClassifier
* DecisionTreeClassifier
* ExtraTreesClassifier
* Support Vector Machine (SVC with StandardScaler)
* XGBoostClassifier (with `scale_pos_weight` for class imbalance)

---

## 📈 Model Evaluation

### Evaluation Metrics Used

* Accuracy
* Confusion Matrix
* Classification Report
* 5-Fold Cross Validation

### Example Performance (Approximate)

| Model         | Accuracy |
| ------------- | -------- |
| Random Forest | ~99%     |
| Decision Tree | ~99%     |
| Extra Trees   | ~99%     |
| SVC           | ~94%     |
| XGBoost       | ~99%     |

⚠ **Note:** The dataset is highly imbalanced (Fraud ≈ 0.2%), so **precision and recall** were also carefully analyzed.

---

## 🏗️ Project Structure

```
online_payments_fraud_detection/
│
├── data/
│   └── PS_20174392719_1491204439457_log.csv
│
├── model/
│   └── payments.pkl
│
├── templates/
│   ├── home.html
│   ├── predict.html
│   └── submit.html
│
├── app.py
├── training.py
└── README.md
```

---

## 🔧 Technical Implementation

### 1️⃣ Data Preprocessing

* Dropped unnecessary columns:

  * `nameOrig`
  * `nameDest`
  * `isFlaggedFraud`
* Label Encoding applied to `type`
* Stratified train-test split (80% training / 20% testing)

---

### 2️⃣ Handling Class Imbalance

* Techniques used:

  * `class_weight='balanced'`
  * `scale_pos_weight` for XGBoost

---

### 3️⃣ Model Saving

```python
pickle.dump(svc, open("model/payments.pkl", "wb"))
```

---

## 🌐 Running the Flask Application

### Step 1: Navigate to project folder

```bash
cd online_payments_fraud_detection
```

### Step 2: Run Flask app

```bash
python app.py
```

### Step 3: Open Browser

```
http://127.0.0.1:5000/
```

---

## 🖥️ Web Application Flow

1. Home Page → Introduction
2. Click **Predict**
3. Enter **7 transaction details**
4. Click **Detect Fraud**
5. View Result:

   * ✅ Not Fraud
   * ⚠ Fraud Transaction

---

## 🔍 Confusion Matrix Meaning

| Term           | Meaning                               |
| -------------- | ------------------------------------- |
| True Positive  | Fraud correctly detected              |
| True Negative  | Normal transaction correctly detected |
| False Positive | Normal transaction marked as fraud    |
| False Negative | Fraud transaction missed              |

---

## 📦 Requirements

Install dependencies:

```bash
pip install pandas numpy scikit-learn flask xgboost
```

Or using requirements file:

```bash
pip install -r requirements.txt
```

---

## ⚠ Important Notes

* Dataset is highly imbalanced
* Accuracy alone is not sufficient for fraud detection
* Precision and Recall are critical evaluation metrics

---

## 📚 Learning Outcomes

* Handling Imbalanced Datasets
* Comparing Multiple Machine Learning Models
* Using Stratified Train-Test Split
* Deploying ML models using Flask
* Building an End-to-End Machine Learning Pipeline

---

## 👥 Contributing

Contributions are welcome!
Please feel free to submit a **Pull Request**.

---

## 📜 License

This project is intended **for educational purposes only**.

---

If you want, I can also:

* Convert this into **GitHub-ready README.md**
* Shorten it for **college project submission**
* Align it with **AICTE / internship documentation**
* Add **screenshots section** or **future scope**

Just tell me 👍
