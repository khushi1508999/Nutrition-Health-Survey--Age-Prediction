# Create the README.md content for the NHANES project
readme_content = """# 👨‍⚕️ Predicting Senior or Adult Using NHANES Dataset

**Hackathon Project | Summer Analytics 2025**  
In collaboration with **Consulting & Analytics Club, IIT Guwahati**

This project leverages a cleaned subset of the **NHANES** dataset to predict whether a U.S. citizen is a **Senior (65+)** or an **Adult (<65)** based on health and lifestyle indicators. The model uses 7 real-world features such as BMI, glucose levels, insulin, and activity response to classify age group with an F1-score as the evaluation metric.

---

## 📂 About the Data

The data contains three CSV files:

- `train.csv` → 2,016 labeled samples (with `age_group`: 0 for Adult, 1 for Senior)  
- `test.csv` → 312 samples to predict  
- `sample-submission.csv` → Format reference for submission

| Feature      | Description                                                              |
|--------------|--------------------------------------------------------------------------|
| SEQN         | Unique respondent ID                                                     |
| RIAGENDR     | Gender (1 = Male, 2 = Female)                                             |
| PAQ605       | Physically active weekly (1 = Yes, 2 = No, 9 = Don't know)               |
| BMXBMI       | Body Mass Index                                                          |
| LBXGLU       | Glucose Level (mg/dL)                                                    |
| DIQ010       | Diabetes diagnosis (1 = Yes, 2 = No, 9 = Don't know)                     |
| LBXGLT       | Oral glucose tolerance test result                                       |
| LBXIN        | Insulin level (μU/mL)                                                    |

---

## 🎯 Objective

Predict whether a respondent is:
- **Adult (0)** → Age < 65  
- **Senior (1)** → Age ≥ 65

Submissions are evaluated on **F1-score**, with tie-breaking based on:
- Feature Engineering
- Exploratory Data Analysis (EDA)

---

## 📊 Approach Summary

- 📌 Handled missing values via imputation
- 📌 Performed label encoding on categorical variables
- 📌 Conducted thorough EDA on BMI, glucose, insulin, and gender distributions
- 📌 Tried classification algorithms including:
  - Logistic Regression
  - Random Forest
  - Gradient Boosting
- 📌 Tuned hyperparameters via GridSearchCV
- 📌 Final predictions submitted as per required format (`sample-submission.csv`)

---

## 🔍 Evaluation & Rules

- Leaderboard is split:
  - **Public**: 50% of test set
  - **Private**: final 50% for final ranking
- Ensure submission format strictly matches `sample-submission.csv`
- Final leaderboard considers marked submissions only

---

## 🛠 Tech Stack

- Python
- NumPy
- Pandas
- scikit-learn
- Seaborn & Matplotlib

---

## 🚀 Getting Started

```bash
git clone https://github.com/your-username/nhanes-age-group-classifier.git
cd nhanes-age-group-classifier
pip install -r requirements.txt
