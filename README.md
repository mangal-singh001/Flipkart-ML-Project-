# Flipkart ML Project

## 📋 Overview

This project analyzes customer support interactions from a Flipkart-like dataset and builds machine learning models to predict Customer Satisfaction (CSAT) scores. The aim is to use data science to learn **what drives satisfaction or dissatisfaction** and create a predictive model that can help the business proactively improve customer experience.

---

## 🧠 Key Features

* Exploratory Data Analysis (EDA): data cleaning, missing values, distributions, visualizations to uncover insights
* Text preprocessing: customer remarks are cleaned, normalized, tokenized, vectorized (TF-IDF)
* Categorical encoding (One-Hot, Label Encoding) & numerical feature transformations (outlier handling, scaling)
* Feature engineering & feature selection: identifying the most impactful features for predicting CSAT
* Multiple ML models built and evaluated (Logistic Regression, Random Forest, XGBoost)
* Hyperparameter tuning to improve model performance
* Model saving (pickle) and sanity check for deployment readiness

---

## 🛠️ Technologies & Tools

* Python (pandas, NumPy)
* Scikit-learn for modeling, preprocessing, splitting, feature selection
* Text processing with NLTK / TF-IDF vectorizer
* XGBoost for the final model
* Pickle to save the model
* Jupyter Notebook for interactive development & visualization

---

## 🔍 Data

* File: `Customer_support_data.csv`
* Roughly **85,000 rows** and **20 columns** (features include: channel, sub‐category, order & response timestamps, agent info, shift, customer remarks, etc.)
* Target variable: `CSAT Score` – takes values 1 through 5

---

## 🚀 Project Structure

```
Flipkart-ML-Project/
│
├── Customer_support_data.csv      # raw data  
├── Sample_EDA_Submission_Template.ipynb    # exploratory data analysis  
├── Sample_ML_Submission_Template.ipynb     # model building, training & evaluation  
├── Flipkart project ppt.pptx        # presentation summarizing insights & model results  
└── README.md                        # this file  
```

---

## ✍️ How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/mangal-singh001/Flipkart-ML-Project-
   ```

2. Ensure you have the required Python packages (example: `requirements.txt`, or install manually):

   ```bash
   pip install pandas numpy scikit-learn xgboost nltk matplotlib seaborn
   ```

3. Open the EDA notebook (`Sample_EDA_Submission_Template.ipynb`) to explore the data and visualizations.

4. Open the ML notebook (`Sample_ML_Submission_Template.ipynb`) to train models, tune parameters, evaluate them, and save the best model.

---

## 📈 Model Performance

| Model                     | Accuracy | Key Strengths                                                                                                                   | Key Weaknesses                                                                              |
| ------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Logistic Regression       | \~37%    | Baseline model, interpretable features, good at detecting some low CSAT cases                                                   | Poor performance for most low/medium CSAT classes; biased toward high CSAT (=5)             |
| Random Forest             | \~36%    | Slightly better balancing, more able to model non‐linear relationships                                                          | Still weak for minority dissatisfaction classes                                             |
| **XGBoost (final model)** | \~69–70% | Best overall accuracy, good handling of major class, stronger F1 / precision / recall on majority class; tuned with hyperparams | Still misses many dissatisfied customers; needs stronger imbalance handling for classes 1–4 |

---

## 🔭 Insights & Business Value

* Major complaints come from **returns**, **delivery delays**, and specific sub-categories.
* Customer remarks text holds signals: negative phrases are associated with low satisfaction.
* Agent shift times and agent tenure also influence CSAT — suggests investment in training / staffing during certain shifts.
* Predictive model lets business actively identify at‐risk customers and prioritize interventions.

---

## 🔐 Deployment Notes

* Final model (XGBoost) saved with Pickle (`.pkl` file)
* Sanity check done on unseen data to verify predictions
* All preprocessing (encoding, scaling, text transformation) is captured so deployment pipeline can replicate it

---

## ⚙️ Next Steps / Improvements

* Use advanced imbalance handling (SMOTE, class weights, focal loss) so low CSAT classes are detected better
* Try other models like LightGBM or ensemble stacking
* Add feature explainability via SHAP for individual predictions to help business users see *why* a customer is predicted dissatisfied
* Build a simple API or dashboard to deploy the model for real use

---

## 📫 Contact

If you're interested in collaborating, discussing improvements, or just want to see more, reach me at:
\[Insert your email or LinkedIn]
