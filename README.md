<h1 align="center">Data Science Projects</h1>

<p align="center">
  Python notebooks from the Springboard Data Science program: statistics, hypothesis testing, machine learning, SQL and data wrangling.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white" alt="Jupyter">
  <img src="https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white" alt="pandas">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white" alt="SciPy">
  <img src="https://img.shields.io/badge/SQL-003B57?style=flat&logo=sqlite&logoColor=white" alt="SQL">
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=flat" alt="Matplotlib">
</p>

---

## About this repo

This repo holds my work from the **Springboard Data Science program (2020-2021)**. It has two capstone projects and more than 20 smaller case studies. Most case studies follow Springboard's guided curriculum. Capstone 2 is my own end-to-end project.

**Jump to:** [Capstones](#capstone-projects) · [Statistics & hypothesis testing](#statistics--hypothesis-testing) · [Machine learning](#machine-learning) · [SQL & data wrangling](#sql-data-wrangling--eda) · [Skills](#skills-at-a-glance)

---

## Capstone projects

### 🏥 Capstone 2: Predicting hospital length of stay at admission

> **Question:** Can we predict how long a patient will stay in hospital, at the moment they are admitted, better than the usual median or average estimate?

| | |
|---|---|
| **Data** | MIMIC-III critical care database (admissions, patients, diagnoses, ICU stays) |
| **Work** | Data cleaning, feature engineering from diagnosis codes and admission details, EDA, model comparison, tuning with GridSearchCV |
| **Models** | Linear Regression, SGD, KNN, Random Forest, Gradient Boosting |
| **Result** | Gradient Boosting performed best (R² about 0.36 before tuning, about 0.38 after). Diagnosis groups like prenatal, respiratory and infectious were the strongest predictors. |
| **Files** | [Proposal](Capstone_2/01_Proposal.pdf) · [Part 1: data & EDA](Capstone_2/Part1_hospital_Length_of_Stay_prediction.ipynb) · [Part 2: modelling](Capstone_2/Part2_hospital_Length_of_Stay_prediction.ipynb) |

<p align="center">
  <img src="Capstone_2/images/compare_models.png" width="48%" alt="Model comparison">
  <img src="Capstone_2/images/feature_importance.png" width="48%" alt="Feature importance">
</p>

### ⛷️ Guided Capstone: Ticket pricing for Big Mountain Resort

> **Question:** What ticket price can Big Mountain Resort support, based on its facilities compared with other resorts?

| | |
|---|---|
| **Data** | Facilities and ticket prices for ski resorts across the US |
| **Work** | Full project cycle in 6 steps: problem statement, wrangling, EDA, preprocessing, modelling, report |
| **Models** | Linear Regression and Random Forest, with cross-validation |
| **Result** | The model suggested a price of about $95.87 vs the current $81 (mean absolute error about $10.39), so there's room for a price increase. I also tested business scenarios, like closing runs or adding a lift, to see the effect on price and revenue. |
| **Files** | [Problem statement](Guided%20Capstone/Step%20one-%20Problem%20Statement) · [Wrangling](Guided%20Capstone/Step%20Two%20-%20Data%20Wrangling/02_data_wrangling.ipynb) · [EDA](Guided%20Capstone/Step%20Three%20-%20Exploratory%20Data%20Analysis/03_exploratory_data_analysis.ipynb) · [Preprocessing](Guided%20Capstone/Step%20Four%20-%20Preprocessing%20and%20Training/04_preprocessing_and_training.ipynb) · [Modelling](Guided%20Capstone/Step%20Five%20-%20Modeling/05_modeling.ipynb) · [Final report (PDF)](Guided%20Capstone/Step%20Six%20-%20Documentation/Report%20for%20Big%20Mountain%20Resort.pdf) |

---

## Statistics & hypothesis testing

| Project | What I did | Methods |
|---|---|---|
| [📱 Apple vs Google app ratings](App_Project/Apps%20project%20_Complete.ipynb) | Tested if app ratings really differ between the two stores and gave a recommendation to the client ([slides](App_Project/App_Project_Presentation.pdf)) | Null and alternative hypotheses, normality test, permutation test |
| [🏥 Hospital charges (Part B)](Frequentist%20Inference/Frequentist%20Inference%20Case%20Study%20-%20Part%20B.ipynb) | Checked if average charges fell below a business threshold, and if insured and uninsured patients are charged differently | Confidence intervals, one- and two-sided tests, t-test |
| [📏 Sampling & confidence intervals (Part A)](Frequentist%20Inference/Frequentist%20Inference%20Case%20Study%20-%20Part%20A.ipynb) | Estimated population values from samples | Central Limit Theorem, z and t critical values, margin of error |
| [📊 Error bars](Error%20Bars/Error%20Bars.ipynb) | Showed uncertainty in charts | Matplotlib error bars |

## Machine learning

**Supervised learning**

| Project | Problem | Methods |
|---|---|---|
| [☕ Specialty coffee](Decision%20Tree%20Specialty%20Coffee%20Case%20Study/Springboard%20Decision%20Tree%20Specialty%20Coffee%20Case%20Study%20-%20Tier%203.ipynb) | Predict which customers will buy a new product | Decision trees |
| [🦠 COVID-19 patients](RandomForest_casestudy_covid19/RandomForest_casestudy_covid19.ipynb) | Predict patient state (isolated, released, deceased) | Random forest |
| [🚢 Titanic](Gradient_Boosting_Case_Study/Gradient%20Boosting%20Case%20Study.ipynb) | Predict passenger survival | Gradient boosting |
| [⚖️ Height & weight](Logistic%20Regression%20Advanced%20Case%20Study/Logistic%20Regression%20Advanced%20Case%20Study.ipynb) | Classify gender from body measurements | Logistic regression, regularization, cross-validation |
| [🏠 Boston housing](Mini_Project_Linear_Regression/Mini_Project_Linear_Regression.ipynb) | Predict house prices | Linear regression, residual analysis |
| [🍷 Red wine quality](Red%20Wine_Regression/Springboard%20Regression%20Case%20Study%20-%20the%20Red%20Wine%20Dataset%20.ipynb) | Predict wine quality from its chemistry | Linear regression, OLS |
| [💉 Diabetes progression](Diabetes/plot_ols.ipynb) | Simple regression example | OLS, R² |
| [📈 Weight-height](weight-height/weight-height.ipynb) | Simple regression example | Linear regression |

**Unsupervised learning & similarity**

| Project | Problem | Methods |
|---|---|---|
| [🛒 Customer segmentation](Clustering_Case_Study/Clustering%20Case%20Study%20-%20Customer%20Segmentation%20with%20K-Means%20-%20Tier%203.ipynb) | Group customers by which marketing offers they responded to | K-Means, elbow method, silhouette score, PCA |
| [📐 Cosine similarity](Cosine_Similarity_Case_Study/CosineSimilarityCaseStudy/Cosine_Similarity_Case_Study.ipynb) | Compare how similar data points are | Cosine similarity |
| [📏 Distance metrics](Euclidean_and_Manhattan_Distances_Case_Study/Euclidean_and_Manhattan_Distances_Case_Study.ipynb) | Compare distance measures | Euclidean and Manhattan distance |

**Model tuning**

| Project | Problem | Methods |
|---|---|---|
| [✈️ Flight delays](Bayesian_Optimization_Case_Study/Bayesian%20Optimization%20Case%20Study/Bayesian_optimization_case_study.ipynb) | Tune a model that predicts flight delays | Bayesian optimization |
| [🩺 Pima diabetes](GridSearchKNN_Case_Study/GridSearchKNN_Case_Study.ipynb) | Find the best KNN settings | Grid search, KNN |

## SQL, data wrangling & EDA

| Project | What I did | Tools |
|---|---|---|
| [🎾 Country club SQL](Country%20Club%20SQL) | Answered business questions on bookings, members and facilities ([queries](Country%20Club%20SQL/SQLTasks.sql)) | SQL, SQLite, Python |
| [🏘️ London housing](London%20Housing/Unit%204%20Challenge%20-%20Tier%203-checkpoint.ipynb) | Found which borough had the biggest price increase over about 20 years | pandas, data cleaning, Matplotlib |
| [☄️ NASA meteorites](NASA%20Meteorite/meteorites.ipynb) | Profiled a public NASA dataset | pandas-profiling |
| [🔍 Pandas profiling](Pandas%20Profiling/Pandas%20Profiling.ipynb) | Automated data quality checks | pandas-profiling |
| [🔗 API data wrangling](api_data_wrangling_mini_project/api_data_wrangling_mini_project2-checkpoint.ipynb) | Pulled stock market data from an API and analyzed it | REST API, JSON, Python |
| [🌐 Web scraping](Web%20Scraping) | Collected and cleaned data from web pages | BeautifulSoup, requests, pandas |
| [🔤 String operations](Vectorized%20String%20Operations/Vectorized%20String%20Operations.ipynb) | Cleaned text data at scale | pandas string methods |
| [🚓 Crime data](DataCamp%20Case%20Studies) | Counted and compared crimes by district | pandas |
| [🏥 Health datasets](hospital-length-of-stay) | Explored hospital datasets while scoping Capstone 2 | pandas, EDA |
| [📘 Python basics](dsc_intro) | NumPy, pandas and Matplotlib basics | Python |

---

## Skills at a glance

| Area | Skills |
|---|---|
| **Statistics** | Hypothesis testing, permutation tests, t-tests, confidence intervals, Central Limit Theorem |
| **Machine learning** | Regression, classification, decision trees, random forest, gradient boosting, KNN, K-Means, PCA |
| **Model evaluation** | Train/test split, cross-validation, R², RMSE, MAE, feature importance, grid search, Bayesian optimization |
| **Data work** | Data cleaning, feature engineering, EDA, data profiling, SQL, APIs, web scraping |
| **Tools** | Python, Jupyter, pandas, NumPy, scikit-learn, SciPy, Matplotlib, Seaborn, SQLite |

## How to run

```bash
git clone https://github.com/bashoori/Data-Science-Projects-Springboard.git
cd Data-Science-Projects-Springboard
pip install pandas numpy scikit-learn scipy matplotlib seaborn jupyter
jupyter notebook
```

Each folder has its own notebook and data. Some datasets come from Kaggle or MIMIC-III and may need to be downloaded separately.

---

## About me

I'm **Bita Ashoori**, a Data Engineer in Vancouver, BC, with 5+ years of experience in ETL, SQL Server, Python and cloud data platforms. These projects are the analytics and machine learning side of my work.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bitaashoori/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/bashoori)
[![Website](https://img.shields.io/badge/Website-bitadigitalhub.com-2E7D32?style=flat)](https://bitadigitalhub.com)
