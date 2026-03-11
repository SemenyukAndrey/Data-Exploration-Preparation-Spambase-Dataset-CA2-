# Data Exploration & Preparation – Spambase (CA2)

> This is an Exploratory Data Analysis (EDA) and data preparation project using the **Spambase** dataset. The main goal is to clean and prepare the data for a machine learning model (a spam filter) and use Principal Component Analysis (PCA) to reduce the number of features while keeping 99.5% of the data's variance.

This project was created for Continuous Assessment 2 (CA2) as part of the **L7 Dip. in Data Analytics** program at CCT College Dublin.

## Project Features

In this project, I went through the full data preparation process before building ML models:
* **Data Overview:** Checking the dataset size, data types, target class distribution (spam vs. non-spam), and finding missing values.
* **Data Cleaning:** Fixing hidden missing values (like `???`, `NA`), converting text to numbers, and filling missing spots with the median to avoid issues with outliers.
* **Feature Scaling:** Using `StandardScaler` to make sure all features are on the same scale. This is required before doing PCA.
* **Exploratory Data Analysis (EDA):** Creating histograms to see how features are distributed and looking at the correlation matrix.
* **Dimensionality Reduction (PCA):** Applying PCA to find the minimum number of features needed to keep 99.5% of the information.
* **Theory:** Explaining the "Curse of Dimensionality" and how it relates to this specific dataset.

## Tech Stack

* **Programming Language:** Python 3
* **Environment:** Jupyter Notebook
* **Main Libraries:** * Data handling: `pandas`, `numpy`
  * Data visualization: `matplotlib`, `seaborn`
  * Machine Learning: `scikit-learn` (`StandardScaler`, `PCA`)

## Repository Structure

* `CA2.ipynb` — The main notebook containing all the code, charts, and explanations.
* `spambase.csv` — The dataset with features of real emails *(make sure it is in the same folder before running the code)*.

## How to Run the Project

If you want to run this project on your local machine, follow these steps:

### 1. Clone the repository
```bash
git clone https://github.com/SemenyukAndrey/Data-Exploration-Preparation-Spambase-Dataset-CA2-.git
```
### 2. Install dependencies
Make sure you have Python installed. Then, install the required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Run the notebook
Open Jupyter Notebook in the project folder:
```bash 
jupyter notebook
```
Open the CA2.ipynb file in your browser and run the cells one by one.

### Key Findings
* The original dataset has 4601 rows (emails) and 59 columns.

* I found 341 missing values in total (including 250 missing values in the word_freq_labs column). I successfully fixed this using median imputation.

* The target variable is_spam is slightly imbalanced: about 60.6% is not spam (False) and 39.4% is spam (True).

* Scaling the data was a very important step. Without it, PCA wouldn't work correctly because the features had completely different ranges.

## Author
Andrii Semeniuk  
Diploma in Data Analytics for Business, CCT College Dublin
