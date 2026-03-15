# 🥤 **CodeX Beverage Pricing Strategy (Classification Model)**

*A portfolio project built as part of the CodeBasics Data Science Virtual Internship*

---

## **Project Overview**

This project is a complete end-to-end **machine learning application** that predicts optimal beverage pricing strategies based on customer demographics, consumption habits, and brand perception.

It was built as part of a simulated industry project with **CodeX**, a leading beverage company, where I take on the role of a Data Scientist tasked with moving the company away from a static pricing model.

The final solution includes:

* Comprehensive data cleaning and validation pipeline
* Exploratory data analysis (EDA) to uncover market segments
* Feature engineering (Zone Affluence Score, Brand Switching Indicator)
* Model training, comparison, and selection (XGBoost)
* A fully functional **Streamlit web app** for real-time pricing strategy simulation

📌 **Live App:** [*CodeX Pricing Strategy App*](https://codexvirtualinternship-bek5wguw53pt9gjhyxqqfc.streamlit.app/)

📌 **GitHub Repo:** [CodeX_Pricing_Strategy](https://github.com/sahilshirodkar30/CodeX_VirtualInternship)

---

# **Business Story: The Pricing Paradox**

**CodeX**, a dominant player in the beverage market, was relying on a "one-size-fits-all" pricing model. This legacy approach created two critical problems:

1. **Lost Margins:** Premium customers in affluent zones were underpriced.
2. **Customer Churn:** Price-sensitive customers in rural areas were overpriced.

**CodeX** engaged the Atliq Data Science team to build an "Intelligence Engine" capable of dynamically segmenting customers and recommending the optimal price bracket.

The project mission:

> *“To transition from static pricing to a dynamic, data-driven revenue model that maximizes margins while retaining market share.”*

This project simulates real-world challenges including handling messy survey data, engineering business-specific features, and deploying a solution that non-technical stakeholders can use.

---

# **Project Objectives**

### **Primary Goal**

Build a classification model to predict the optimal price range for a customer and deploy it as an interactive dashboard.

### **Key Success Metrics**

* **Accuracy:** Achieve >85% prediction accuracy on test data.
* **Segment Identification:** Successfully differentiate between "Premium" and "Value" customers.
* **Usability:** Deliver a no-code interface for the Strategy Team.

---

# **Project Structure**

```
CodeX_VirtualInternship
│
├── app/                         # Streamlit web application
│   ├── main.py                  # Dashboard UI & Logic
│   ├── prediction_helper.py     # Inference pipeline & feature engineering
│   ├── test.py          
│
├── models/                      # Model Training Artifacts (Backup)
│   ├── model_columns.pkl
│   └── model_data.pkl
│
├── notebooks/                   # Jupyter Notebooks for analysis
│   └── final_documents.ipynb      # End-to-End: Cleaning, EDA, Feature Eng., Modeling
│
├── .gitignore                   # Excludes raw data & cache
├── requirements.txt             # Dependencies
└── README.md

```

---

# **Technical Stack**

### **Languages & Libraries**

* **Python 3.9+**
* **Pandas, NumPy:** Data manipulation & processing
* **Scikit-Learn:** Preprocessing & baseline models
* **XGBoost:** High-performance gradient boosting classification
* **LightGBM, Random Forest:** Model comparison
* **Plotly:** Interactive visualizations
* **Streamlit:** Application deployment framework
* **Joblib:** Model serialization

---

# **Model Overview**

The pricing strategy was treated as a **multi-class classification problem**.

| **Algorithm** | **Accuracy** | **Status** |
| --- | --- | --- |
| **XGBoost** | **92.19%** | ✅ **Selected** |
| LightGBM | 92.01% | Runner-up |
| Random Forest | 89.36% | Strong Baseline |
| Support Vector Machine (SVM) | 82.37% | Moderate Performance |
| Logistic Regression | 80.09% | Baseline |
| Gaussian Naive Bayes | 52.14% | Discarded |

**Feature Engineering Highlights:**

* **`ZAS_Score` (Zone Affluence Score):** A composite metric combining City Tier (Metro/Rural) and Income Level.
* **`BSI` (Brand Switching Indicator):** Identifies customers likely to churn based on "Price" or "Quality" concerns.
* **`Consumption_Score`:** Ratio of purchase frequency to brand awareness.

---

# **Streamlit App**

The Streamlit dashboard allows the Strategy Team to simulate customer personas.

**Key Features:**
✔ **Scenario Planning:** Input distinct profiles (e.g., "Rural Student" vs. "Metro Professional").
✔ **Instant Prediction:** Returns the optimal price bracket (e.g., ₹50-100 vs. ₹150-200).
✔ **Probability Distribution:** Shows model confidence across all price bands.
✔ **Business Insight:** Automatically generates a strategic summary based on the prediction.

## Application Preview

📌 **Live App:** [*CodeX Pricing Strategy App*](https://codexvirtualinternship-v4gqjrsqeokmnhauoatoaj.streamlit.app/)


---


# **How to Run Locally**

### 1. Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/CodeX_Pricing_Strategy.git
cd CodeX_Pricing_Strategy

```

### 2. Install dependencies

```bash
pip install -r requirements.txt

```

### 3. Run the Streamlit app

```bash
streamlit run app/main.py

```

---

# **Learnings from the Project**

* **Data Integrity:** Real-world survey data is messy. I learned robust cleaning techniques for categorical inconsistencies and logical outliers.
* **Feature Power:** The jump in accuracy from 80% to 92% was driven by engineered features (`ZAS_Score`), not just model tuning.
* **Deployment:** Moving a model from a Jupyter Notebook to a functional web app requires rethinking code structure for inference efficiency.

---

# **Acknowledgements**

* **CodeBasics** for the project framework and dataset access.
* **CodeX (Simulated Client)** for the business context and requirements.

---

# **Author**

**Sahil Shirodkar**

Data Science Virtual Intern @ CodeBasics

---


