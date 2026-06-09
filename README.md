# 🩺 Diabetes Prediction using Machine Learning

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://diabetespredicationdsp.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

A Machine Learning powered web application that predicts whether a person is diabetic or not based on key health parameters. Built with **Streamlit** and trained on the **PIMA Indians Diabetes Dataset**.

🔗 **Live App:** [https://diabetespredicationdsp.streamlit.app/](https://diabetespredicationdsp.streamlit.app/)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [ML Model](#ml-model)
- [Input Parameters](#input-parameters)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Deployment](#deployment)
- [Technologies Used](#technologies-used)

---

## 🔍 Overview

This project uses a pre-trained Machine Learning classification model to predict diabetes risk. Users select their health values from dropdowns populated directly from the dataset, and the app instantly predicts whether the person is **diabetic** or **not diabetic**.

---

## ✨ Features

- 🎯 **Instant Prediction** — Click one button to get the result
- 📊 **Data-Driven Dropdowns** — All input values are sourced from the real dataset (no manual typing)
- 🧠 **Pre-trained ML Model** — Fast, accurate predictions using a saved `joblib` model
- 📱 **Responsive 3-Column Layout** — Clean, organized UI
- ☁️ **Live on Streamlit Cloud** — Accessible from any browser, no installation needed

---

## 📂 Dataset

**PIMA Indians Diabetes Dataset**

| Property | Details |
|---|---|
| File | `diabetes.csv` |
| Source | [Kaggle / UCI ML Repository](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) |
| Records | 768 rows |
| Features | 8 input features + 1 target (Outcome) |
| Classes | 0 = Not Diabetic, 1 = Diabetic |

---

## 🤖 ML Model

- **Algorithm:** Support Vector Classifier (SVC)
- **Model file:** `diabetes` (saved via `joblib`)
- **Trained in:** `dibetes_main.ipynb`
- The notebook covers data preprocessing, model training, evaluation, and export

---

## 📊 Model Performance

<div align="center">

### 🏆 Overall Scores

| | Metric | Score | Visual |
|:---:|:---|:---:|:---|
| 🟢 | **Accuracy** | **82.12%** | `████████░░` 82% |
| 🔵 | **Precision** | **74.04%** | `███████░░░` 74% |
| 🟡 | **Recall** | **57.46%** | `█████░░░░░` 57% |
| 🟣 | **F1 Score** | **64.71%** | `██████░░░░` 65% |

</div>

---

### 📋 Detailed Classification Report

| Class | Precision | Recall | F1-Score | Support |
|:---|:---:|:---:|:---:|:---:|
| 🟩 **0 — Not Diabetic** | `80%` | `89%` | `84%` | 500 |
| 🟥 **1 — Diabetic** | `74%` | `57%` | `65%` | 268 |
| ⬛ **Weighted Average** | **`78%`** | **`78%`** | **`77%`** | **768** |

> 💡 **Model:** SVC trained on 768 samples with 8 health features. Achieves **78% accuracy** on the PIMA Indians Diabetes Dataset.



## 🧾 Input Parameters

| Parameter | Description | Type |
|---|---|---|
| **Pregnancies** | Number of times pregnant | Integer |
| **Glucose** | Plasma glucose concentration (mg/dL) | Integer |
| **Blood Pressure** | Diastolic blood pressure (mm Hg) | Integer |
| **Skin Thickness** | Triceps skinfold thickness (mm) | Integer |
| **Insulin** | 2-Hour serum insulin (μU/mL) | Integer |
| **BMI** | Body Mass Index (weight in kg / height in m²) | Float |
| **Diabetes Pedigree Function** | Diabetes likelihood based on family history | Float |
| **Age** | Age of the person (years) | Integer |

---

## 📁 Project Structure

```
Diabetes_Predication/
│
├── streamlit.py            # Main Streamlit web application
├── diabetes                # Pre-trained ML model (joblib format)
├── diabetes.csv            # PIMA Indians Diabetes Dataset
├── dibetes_main.ipynb      # Jupyter notebook — data analysis & model training
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/dsp515/Suger-Test.git
cd Suger-Test
```

### 2. Create a virtual environment (recommended)
```bash
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # Mac/Linux
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

Run the Streamlit app locally:

```bash
streamlit run streamlit.py
```

Then open your browser at **http://localhost:8501**

### How to use:
1. Select your health values from each dropdown
2. Click **"Diabetes Test Result"**
3. The app displays: **"The person is diabetic"** or **"The person is not diabetic"**

---

## ☁️ Deployment

This app is deployed on **Streamlit Community Cloud**.

| Setting | Value |
|---|---|
| Repository | `dsp515/Suger-Test` |
| Branch | `main` |
| Main file | `streamlit.py` |
| Live URL | https://diabetespredicationdsp.streamlit.app/ |

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python 3.8+ | Programming language |
| Streamlit | Web application framework |
| scikit-learn | Machine learning model |
| pandas | Data loading & manipulation |
| joblib | Model serialization/loading |
| numpy | Numerical computation |
| Jupyter Notebook | Model training & EDA |

---

## ⚠️ Disclaimer

This application is built for **educational purposes only**. The predictions made by this model should **NOT** be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult a qualified healthcare provider.

---

> ⭐ If you found this project helpful, please give it a star on GitHub!
