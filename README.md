# Banknotes-Authentication
# 🏦 Banknote Authentication using Decision Tree

## 📌 Project Overview

This project uses a **Decision Tree Classification** algorithm to identify whether a banknote is **genuine or counterfeit** based on statistical features extracted from images of banknotes.

The trained Decision Tree model is saved as a `.pkl` file and can be used for making predictions on new banknote data.

---

## 🎯 Objective

The main objective of this project is to build a machine learning classification model that can distinguish between:

* **0 → Genuine Banknote**
* **1 → Counterfeit Banknote**

The prediction is based on four numerical features extracted from banknote images.

---

## 📊 Dataset

The dataset contains **1,372 records** and the following 5 columns:

| Feature  | Description                               |
| -------- | ----------------------------------------- |
| Variance | Variance of the Wavelet Transformed image |
| Skewness | Skewness of the Wavelet Transformed image |
| Curtosis | Curtosis of the Wavelet Transformed image |
| Entropy  | Entropy of the image                      |
| Class    | Target variable                           |

### Input Features

```text
Variance
Skewness
Curtosis
Entropy
```

### Target

```text
Class
```

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib
* Streamlit

---

## 🔄 Machine Learning Workflow

```text
Dataset
   ↓
Data Analysis
   ↓
Data Preprocessing
   ↓
Feature Selection
   ↓
Train-Test Split
   ↓
Decision Tree Classifier
   ↓
Model Evaluation
   ↓
Save Model as .pkl
   ↓
Deployment
```

---

## 🌳 Decision Tree Algorithm

A Decision Tree is a supervised machine learning algorithm used for both classification and regression.

For classification, the algorithm creates a tree-like structure by splitting the dataset based on feature values. Each decision node represents a condition, and the final leaf node represents the predicted class.

In this project, a **Decision Tree Classifier using Gini impurity** is used.

---

## 📐 Gini Impurity

Gini impurity measures how mixed the classes are within a node.

The Decision Tree selects splits that reduce the impurity of the data.

The Gini impurity formula is:

```text
Gini = 1 - Σ(pᵢ)²
```

where `pᵢ` represents the probability of a particular class.

---

## 🤖 Model

The trained model is a:

```text
DecisionTreeClassifier
```

The saved model file is:

```text
decision_tree_gini.pkl
```

The model uses `random_state=42`.

---

## 💾 Model Saving

The trained model can be saved using Joblib:

```python
import joblib

joblib.dump(model, "decision_tree_gini.pkl")
```

The saved `.pkl` file can then be loaded for prediction:

```python
model = joblib.load("decision_tree_gini.pkl")
```

---

## 🌐 Deployment

The trained model can be deployed using **Streamlit**.

The user can enter the four banknote features:

```text
Variance
Skewness
Curtosis
Entropy
```

The application passes these values to the trained Decision Tree model and displays the predicted class.

---

## 📁 Project Structure

```text
Banknote_Authentication/
│
├── app.py
├── decision_tree_gini.pkl
├── banknotes.csv
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## 📦 Requirements

Create a `requirements.txt` file containing:

```text
pandas
numpy
scikit-learn
joblib
streamlit
matplotlib
seaborn
```

---

## ▶️ Run the Application

After installing the required libraries, run:

```bash
streamlit run app.py
```

The Streamlit application will open in the browser.

---

## 🖥️ Application Input

The application accepts:

```text
Variance
Skewness
Curtosis
Entropy
```

After entering the values, click the **Predict** button.

The model will classify the banknote into its corresponding class.

---

## 📈 Model Evaluation

The model can be evaluated using:

* Accuracy
* Confusion Matrix
* Precision
* Recall
* F1 Score
* Classification Report

These metrics help determine how well the Decision Tree model distinguishes between the two banknote classes.

---

## 📚 Key Learning Outcomes

Through this project, I learned:

* Data analysis using Pandas
* Feature selection
* Classification using Decision Trees
* Gini impurity
* Train-test splitting
* Model evaluation
* Confusion matrix
* Classification report
* Model serialization using Joblib
* Machine learning model deployment using Streamlit

---

## 👩‍💻 Project Details

**Author:** Aditi Tawade

**Guide:** Yameen Hakim Sir

**Degree:** B.Tech — Electronics & Telecommunication Engineering

---

## ⭐ Conclusion

This project demonstrates an end-to-end machine learning workflow for **banknote authentication**, from dataset analysis and model training to saving the trained Decision Tree model and deploying it for predictions.

The project provides practical experience in **machine learning classification, model evaluation, and deployment**.
