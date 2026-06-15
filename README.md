# Airline Passenger Satisfaction ML Analysis

A machine learning analysis identifying the service, travel, and operational factors that influence airline passenger satisfaction.

This project uses Python and scikit-learn to analyze airline passenger satisfaction data, perform exploratory data analysis, preprocess features, train classification models, compare model performance, and identify the strongest drivers of customer satisfaction.

---

## Project Overview

Airline customer satisfaction is a major business problem because unhappy passengers can lead to lost loyalty, negative reviews, and reduced competitive advantage.

The goal of this project was to answer:

> What factors most strongly influence whether an airline passenger is satisfied or dissatisfied?

The analysis focuses on features such as travel type, class, in-flight WiFi, online boarding, seat comfort, check-in service, delays, and other passenger experience factors.

---

## Business Problem

In a highly competitive airline industry, customer satisfaction is directly connected to retention, loyalty, and brand reputation.

By identifying the factors that most influence satisfaction, airlines can make better decisions about:

* Service improvements
* Customer segmentation
* In-flight experience upgrades
* Delay reduction
* Marketing and loyalty strategies

---

## Dataset

The project uses an airline passenger satisfaction dataset with separate train and test files.

For exploratory analysis, the train and test datasets were combined to analyze overall satisfaction patterns. The target variable is passenger satisfaction, encoded as:

* `Satisfied` → 1
* `Neutral or Dissatisfied` → 0

The dataset includes features related to:

* Demographics
* Type of travel
* Travel class
* Flight distance
* In-flight WiFi service
* Online boarding
* Seat comfort
* Food and drink
* Cleanliness
* Check-in service
* Baggage handling
* Departure delay

---

## Tools and Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Logistic Regression
* Decision Tree Classifier
* LabelEncoder
* StandardScaler
* ROC/AUC Analysis

---

## Notebook Workflow

The notebook follows this structure:

1. Load train and test datasets
2. Combine datasets for exploratory data analysis
3. Clean and inspect the data
4. Encode categorical variables
5. Standardize numerical features for Logistic Regression
6. Train a Logistic Regression model
7. Train a Decision Tree model
8. Compare model performance
9. Analyze feature importance
10. Generate business recommendations

---

## Exploratory Data Analysis

The EDA explored how satisfaction changes across different passenger and service categories.

Key findings included:

* Business Class passengers showed higher satisfaction than Economy and Eco Plus passengers.
* Business travelers were generally more satisfied than personal travelers.
* Online boarding, in-flight WiFi, travel type, and class were strong satisfaction drivers.
* Departure delays negatively affected passenger satisfaction.
* Some features, such as gate location and food/drink, appeared to have weaker influence on overall satisfaction.

---

## Models Used

### Logistic Regression

Logistic Regression was used as a baseline classification model. Since it is a linear model, numerical features were standardized before training.

The model provided interpretable coefficients and helped identify which features had strong positive or negative relationships with passenger satisfaction.

### Decision Tree Classifier

A Decision Tree Classifier was used to capture non-linear relationships between passenger experience features and satisfaction.

The Decision Tree performed better than Logistic Regression, suggesting that passenger satisfaction depends on combinations of factors rather than only simple linear relationships.

---

## Model Performance

The project compared Logistic Regression and Decision Tree performance using standard classification metrics.

### Logistic Regression

* Accuracy: 0.8710
* Precision: 0.8678
* Recall: 0.8331
* F1 Score: 0.8501

### Decision Tree

* Accuracy: 0.9465
* Precision: 0.9374
* Recall: 0.9408
* F1 Score: 0.9391

The Decision Tree model outperformed Logistic Regression, especially in overall accuracy and ROC/AUC comparison.

---

## Key Predictive Features

The strongest satisfaction drivers included:

* Online boarding
* In-flight WiFi service
* Type of travel
* Travel class
* Seat comfort
* Check-in service

These features suggest that passenger satisfaction is heavily influenced by digital experience, service quality, and travel context.

---

## Business Recommendations

Based on the analysis, airlines should focus on:

### 1. Improve In-Flight Amenities

Upgrade in-flight WiFi, seat comfort, and related onboard services, especially for lower-tier classes.

### 2. Reduce Delays

Departure delays negatively affect satisfaction, so operational improvements around punctuality can improve customer experience.

### 3. Segment Customers

Business and personal travelers have different expectations. Airlines should tailor services and offers based on travel type.

### 4. Improve Digital Experience

Online boarding was one of the strongest predictors of satisfaction, suggesting that digital touchpoints are critical to the customer journey.

---

## Project Files

Recommended repository structure:

```text
airline-passenger-satisfaction-ml/
│
├── README.md
├── notebooks/
│   └── airline_passenger_satisfaction_ml_analysis.ipynb
├── presentation/
│   └── airline_passenger_satisfaction_ml_presentation.pdf
└── images/
    └── thumbnail.png
```

---

## How to Run the Notebook

1. Clone the repository:

```bash
git clone https://github.com/your-username/airline-passenger-satisfaction-ml.git
cd airline-passenger-satisfaction-ml
```

2. Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

3. Open the notebook:

```bash
jupyter notebook notebooks/airline_passenger_satisfaction_ml_analysis.ipynb
```

4. Run all cells from top to bottom.

---

## Future Improvements

Possible improvements include:

* Add Random Forest or Gradient Boosting models
* Tune Decision Tree depth and pruning parameters
* Use cross-validation for more robust model evaluation
* Add SHAP values for better model interpretability
* Build a small Streamlit dashboard
* Deploy a simple prediction API using FastAPI
* Add a cleaned reusable Python script version of the notebook

---

## Author

Yajat Mehta
Data Analytics & AI
GitHub: mehtaversehq
