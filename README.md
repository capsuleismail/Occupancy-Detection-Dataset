# Room Occupancy Prediction — EDA & Model Comparison

## Overview.
This project investigates a sensor-based dataset to predict room occupancy using machine learning.  
It combines **exploratory data analysis (EDA)**, **feature engineering**, and **model comparison** to understand what drives occupancy and build reliable predictions.

---

## Objectives.
- Identify the most predictive features
- Understand data patterns and distributions
- Detect multicollinearity
- Apply appropriate preprocessing
- Compare multiple machine learning models
- Evaluate model performance using suitable metrics

---

## Dataset.
The dataset contains environmental sensor readings used for **binary classification (occupied vs not occupied)**.

**Features:**
- Temperature  
- Humidity  
- Light  
- CO₂  
- Humidity Ratio  

Ground truth occupancy was obtained from **time-stamped images taken every minute**.

---

## Exploratory Data Analysis (EDA)

During the following project I had a serious of question answered and explained on my notebook, such as:

- Which features are most predictive of occupancy?
- Why is light such a dominant feature?
- Curious Insight.
- How a Cyclical Encoding can improve our model accuracy?
- How would you check for multicollinearity (VIF and Correlation Plot)?
- Is the dataset balanced?
- Which evaluation metrics are most appropriate?
- How the values are distributed?
- What preprocessing step are needed?
- What models are going to execute and why?
- Should date/time be used as a feature?
- What model perform best on this dataset?
- What feature engineering could improve results?
- What real-world issues could affect model reliability?

### Dataset not Balanced
The dataset is relatively imbalanced, with a 76,90% over 23,10% proportion.

### Multicollinearity
Correlation analysis and VIF revealed high correlation between some variables (e.g. humidity-related features), indicating multicollinearity.

---

## Preprocessing
- Cleaned inconsistent data types (object → numeric)
- Checked for missing or incorrect values
- Scaled numerical features and applied Principal Components Analysis (PCA)
- Removed or handled correlated variables
- Engineered time-based features using cyclical encoding (sin/cos)
- 

---

## Feature Engineering
- Cyclical encoding improved model performance by capturing time-based patterns
- Consideration of whether to include datetime features
- Handling redundant features due to multicollinearity

---

## Models Implemented
- Logistic Regression  
- Random Forest  
- XGBoost  

These models were selected to compare **linear vs non-linear approaches**.

---

## Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC-AUC  

ROC-AUC was used as the primary metric for comparison.
