# Customer Churn Prediction

A machine learning project that predicts whether a telecom customer is likely to churn based on customer demographics, services, contract details, and billing information.

## Project Overview

Customer churn refers to customers leaving a service provider.

The goal of this project is to build a machine learning model that can identify customers who are likely to churn. The project includes data preprocessing, exploratory data analysis, model comparison, model evaluation, and a Streamlit web application for making predictions.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Streamlit
* Jupyter Notebook

## Machine Learning Models

Three classification models were evaluated:

1. Logistic Regression
2. Random Forest
3. Gradient Boosting

The models were compared using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

The final model is a Logistic Regression pipeline containing preprocessing and classification.

## Model Performance

| Metric          |  Score |
| --------------- | -----: |
| Accuracy        | 80.38% |
| Churn Precision |    65% |
| Churn Recall    |    57% |
| Churn F1-Score  |    61% |
| ROC-AUC         |  0.836 |

The model achieved approximately **80% accuracy** and a **ROC-AUC of 0.836** on the test set.

## Project Structure

```text
customer-churn-prediction/
│
├── app/
│   └── app.py
│
├── data/
│
├── models/
│   └── churn_model.pkl
│
├── notebooks/
│   └── 01_customer_churn_eda.ipynb
│
├── src/
│
├── .gitignore
├── requirements.txt
└── README.md
```

## Dataset

The project uses the Telco Customer Churn dataset.

The dataset contains information about:

* Customer demographics
* Tenure
* Phone services
* Internet services
* Online services
* Contract type
* Payment method
* Monthly charges
* Total charges
* Customer churn

The `customerID` column was removed because it is an identifier and does not provide useful predictive information.

## Data Preprocessing

The following preprocessing steps were performed:

* Converted `TotalCharges` to numeric format
* Handled missing values
* Removed the `customerID` identifier
* Converted the target variable `Churn` into binary values

  * `No = 0`
  * `Yes = 1`
* Applied StandardScaler to numerical features
* Applied OneHotEncoder to categorical features
* Used a train-test split with stratification

## Streamlit Application

The project includes an interactive Streamlit application.

The application allows users to enter customer information such as:

* Tenure
* Monthly charges
* Total charges
* Contract
* Internet service
* Payment method
* Customer services

The application then predicts:

* Whether the customer is likely to churn
* The estimated churn probability

## How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
cd customer-churn-prediction
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the virtual environment

On Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 5. Run the Streamlit application

```bash
python -m streamlit run app/app.py
```

The application will open in your browser.

## Future Improvements

Possible improvements include:

* Hyperparameter tuning
* Cross-validation
* Feature importance analysis
* Threshold optimization for churn detection
* Model monitoring
* Deployment to a cloud platform
* Adding a dashboard for churn analysis
* Adding customer retention recommendations

## Author

**Sara Waghchaure**

B.Tech — Computer Science Engineering
Artificial Intelligence & Data Science
