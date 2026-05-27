# 🛍️ Customer Segmentation for E-Commerce Using Machine Learning

A machine learning project that segments e-commerce customers into meaningful groups using clustering algorithms — enabling targeted marketing, personalized recommendations, and improved customer retention.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Dataset](#dataset)
- [How It Works](#how-it-works)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Results](#results)
- [License](#license)

---

## 📖 Overview

Customer segmentation divides customers into groups based on shared characteristics such as purchasing behavior and transaction history. This project applies unsupervised machine learning (K-Means Clustering with RFM Analysis) to an e-commerce dataset to identify distinct customer segments and visualize insights through an interactive app.

---

## ✨ Features

- Data preprocessing & cleaning on real e-commerce data
- Exploratory Data Analysis (EDA) with attribute histograms
- RFM (Recency, Frequency, Monetary) feature engineering
- K-Means Clustering for customer segmentation
- Saved model artifacts (`.pkl`) for reuse
- Interactive web app (`app.py`) for predictions

---

## 🛠️ Tech Stack

- **Language:** Python 3.x
- **Libraries:**
  - `pandas`, `numpy` — Data manipulation
  - `matplotlib`, `seaborn` — Data visualization
  - `scikit-learn` — Machine learning (KMeans, preprocessing)
  - `streamlit` or `flask` — Web app (`app.py`)
  - `jupyter` — Notebook-based analysis
  - `pickle` — Model serialization

---

## 📊 Dataset

- **File:** `customer.xlsx` (~23 MB)
- Contains transactional e-commerce data including customer IDs, purchase history, quantities, and prices.

---

## ⚙️ How It Works

1. **Data Cleaning** — Handle missing values, remove duplicates, filter invalid transactions
2. **Feature Engineering** — Compute RFM scores per customer from `customer.xlsx`
3. **Preprocessing** — Scale features using StandardScaler
4. **Clustering** — Apply K-Means; determine optimal K using Elbow Method
5. **Save Model** — Export average cluster values to `avg_values.pkl`
6. **Web App** — `app.py` loads the model and lets users interact with predictions

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/KunjanNandha/CUSTOMER-SEGMENTATION-FOR-E-COMMERCE-USING-MACHINE-LEARNING-ALGORITHM.git
cd CUSTOMER-SEGMENTATION-FOR-E-COMMERCE-USING-MACHINE-LEARNING-ALGORITHM
```

### 2. Create & Activate Virtual Environment

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# Mac/Linux
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

> Or install manually:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn streamlit openpyxl jupyter
```

### 4. Run the Jupyter Notebook

```bash
jupyter notebook Main.ipynb
```

### 5. Run the Web App

```bash
# Check the Run.txt file for exact command, or try:
streamlit run app.py
```

---

## 📁 Project Structure

```
Customer Segmentation/
│
├── .venv/                        # Virtual environment
├── Main.ipynb                    # Main Jupyter notebook (EDA + ML)
├── app.py                        # Web app for customer segmentation
├── customer.xlsx                 # E-commerce dataset (23 MB)
├── avg_values.pkl                # Saved model cluster averages
├── Histograms of Attributes.png  # EDA visualization
└── Run.txt                       # Instructions to run the project
```

---

## 📈 Results

Customers are grouped into segments such as:

| Cluster | Label            | Characteristics                             |
|---------|------------------|----------------------------------------------|
| 0       | High-Value       | Recent, frequent buyers with high spend      |
| 1       | At-Risk          | Previously active but haven't bought lately  |
| 2       | New Customers    | Recently acquired, low frequency             |
| 3       | Loyal Customers  | Frequent buyers, moderate spend              |

**Sample visualization from the project:**

![Histograms of Attributes](Histograms%20of%20Attributes.png)

---

## 👤 Author

**Kunjan Nandha**
[GitHub Profile](https://github.com/KunjanNandha)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
