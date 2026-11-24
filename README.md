# Titanic: Data Cleaning \& Exploratory Data Analysis

Cleaning and exploring the Kaggle Titanic dataset to find out which factors influenced survival.

## What's inside

* `titanic\_eda.ipynb`: full analysis (cleaning, univariate, bivariate and multivariate EDA, findings)
* `data/train.csv`: Kaggle Titanic training data (891 passengers)

## Cleaning steps

|Issue|Treatment|
|-|-|
|`Age` missing (20%)|Filled with the median age per title extracted from `Name`|
|`Cabin` missing (77%)|Converted to `HasCabin` and `Deck` features, original column dropped|
|`Embarked` missing (2)|Filled with the mode|
|`Fare` skewed, outliers|Added `LogFare`|
|New features|`Title`, `FamilySize`, `IsAlone`, `AgeGroup`|

## Key findings

* Women survived at **74%** vs **19%** for men.
* Survival fell with class: **63%** (1st), **47%** (2nd), **24%** (3rd).
* Class and sex interact: 1st-class women survived at 97%, 3rd-class men at 13.5%.
* Children (0-12) survived at 58%; passengers over 60 at 23%.
* Small families (2-4) did best; solo travelers and large families did worse.
* Overall survival rate: 38.4%.

## Run it

```bash
git clone <https://github.com/karan26612/SCT\_DS\_2>
cd titanic-eda
pip install -r requirements.txt
jupyter notebook titanic\_eda.ipynb
```

## Tech

Python, pandas, NumPy, Matplotlib, Seaborn.

## Data source

[Kaggle: Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic)
