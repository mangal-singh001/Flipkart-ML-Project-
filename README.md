# 📦 Flipkart ML Project

## 📋 Overview

This project was developed as part of my **first-week task during the Labmentix Internship**.
The goal was to analyze customer support interactions from a Flipkart-like dataset and build machine learning models to predict **Customer Satisfaction (CSAT)** scores.

The project highlights how **data science can uncover key drivers of satisfaction/dissatisfaction** and create predictive models that help businesses proactively improve customer experience.

---

## 🧠 Key Features

* 📊 **EDA**: Cleaning, missing values handling, duplicates check, visualizations to uncover insights
* 📝 **Text Preprocessing**: Customer remarks cleaning, normalization, tokenization, TF-IDF vectorization
* 🔑 **Categorical Encoding**: One-Hot, Label Encoding (low, medium & high cardinality features)
* 🛠️ **Feature Engineering**: Outlier handling, feature selection (Chi-Square, ANOVA, Random Forest)
* ⚖️ **Imbalance Handling**: SMOTE applied for minority CSAT classes
* 🤖 **ML Models**: Logistic Regression, Random Forest, XGBoost (final model)
* 🎯 **Hyperparameter Tuning**: GridSearchCV for optimization
* 💾 **Deployment Ready**: Best model saved using Pickle and tested on unseen data

---

## 🛠️ Tech Stack

* **Languages/Libraries**: Python, pandas, NumPy, scikit-learn, XGBoost, NLTK, matplotlib, seaborn
* **ML Workflow**: Preprocessing → Feature Engineering → Model Training → Hyperparameter Tuning → Deployment

---

## 🔍 Dataset

* \~85,000 records and 20 columns
* Features: Channel, Category, Sub-category, Agent details, Customer remarks, Order details, etc.
* Target: `CSAT Score` (1 to 5)

---

## 🚀 Project Structure

```
Flipkart-ML-Project/
│
├── Customer_support_data.csv                # Dataset
├── Sample_EDA_Submission_Template.ipynb     # EDA Notebook
├── Sample_ML_Submission_Template.ipynb      # ML Modeling Notebook
├── Flipkart project ppt.pptx                # Presentation slides
└── README.md                                # Project documentation
```

---

## 📈 Model Performance

| Model               | Accuracy | Highlights 🚀                              | Limitations ⚠️                      |
| ------------------- | -------- | ------------------------------------------ | ----------------------------------- |
| Logistic Regression | \~37%    | Interpretable baseline                     | Weak on minority CSAT classes       |
| Random Forest       | \~36%    | Better with non-linear data                | Still biased towards majority class |
| **XGBoost (Final)** | \~69%    | Best accuracy & F1, strong business impact | Needs better handling for low CSAT  |

---

## 🔭 Insights & Business Impact

* 📌 **Returns & delivery delays** are the most common causes of dissatisfaction
* ⏳ Longer handling times often correlate with lower CSAT
* 📞 Channel performance varies: inbound dominates but emails show mixed results
* 👩‍💼 Agent tenure & shift influence satisfaction — training & scheduling improvements can boost scores
* 🚀 Predicting CSAT in advance allows prioritizing **at-risk customers**, reducing churn and improving retention

---

## 🔐 Deployment

* ✅ Final model: **XGBoost**
* ✅ Saved using Pickle (`model.pkl`)
* ✅ Tested on unseen data for sanity check
* 🔮 Ready to be integrated with dashboards or APIs

---

## ⚙️ Future Improvements

* 🔄 Better imbalance handling (focal loss, cost-sensitive learning)
* 🌍 Deploy as an API with FastAPI/Flask
* 📊 Use SHAP/LIME for model explainability
* ⚡ Try LightGBM or ensemble stacking for higher accuracy

---

## 📫 Contact

👨‍💻 **Mangal Singh**
🔗 [LinkedIn](https://www.linkedin.com/in/mangal-singh001)
🐙 [GitHub](https://github.com/mangal-singh001)

---

