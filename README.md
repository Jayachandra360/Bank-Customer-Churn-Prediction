# Bank-Customer-Churn-Prediction

# Bank Customer Churn Prediction - README

Project Overview
This project aims to predict customer churn (whether a customer will leave the bank) using machine learning models such as  Logistic Regression, Random Forest, and Neural Networks . The dataset contains customer details and their churn status, with features such as credit score, balance, geography, and activity status.

Data Processing:
1.  Loaded the dataset  from Google Drive.
2.  Dropped irrelevant columns :
   - `RowNumber`, `CustomerId`, and `Surname` as they do not contribute to predictive modeling.
3.  Handled categorical variables :
   - Converted `Gender` to numerical (Male = 1, Female = 0).
   - Used one-hot encoding for `Geography` (France, Germany, Spain).
4.  Checked for missing values , none were found.
5.  Standardized numerical features  using `StandardScaler`.
6.  Split data  into  training (80%) and testing (20%)  sets.
7.  Balanced the dataset  using  SMOTE  to handle class imbalance.

Exploratory Data Analysis (EDA):
-  Churn distribution : About  20%  of customers have churned.
-  Gender & Churn :
  -  Females  have a slightly higher churn rate (~25%) than males (~16%).
-  Age & Churn :
  - Older customers  (45+)  are more likely to churn.
-  Geography & Churn :
  - Customers from  Germany  have the highest churn rate (~32%).
-  Credit Score & Churn :
  - Customers with  lower credit scores  tend to churn more.
-  Balance & Churn :
  - Customers with  higher balances  are more likely to churn.
-  Activity & Churn :
  -  Active members  are less likely to churn.

Hidden Patterns & Insights:
1.  Age is the Most Important Factor 
   - Older customers (45+) have a significantly higher chance of leaving the bank.
   - The model shows that  Age is the strongest predictor  of churn.

2.  High Balance = Higher Churn?  🤔
   - Customers with  zero balance  tend to  stay .
   - Customers with  mid-to-high balances  have a higher churn rate.
   - Possible reason: These customers may have savings elsewhere or are considering better banking options.

3.  Geography Matters  🌍
   - German customers  churn more frequently .
   - French and Spanish customers are more stable.
   - Possible reason: Different banking policies or competition in Germany.

4.  Number of Products & Churn  📊
   - Customers with  1 or 2 products  tend to stay.
   - Customers with  3 or more products  have a higher churn rate.
   - Maybe they signed up for extra services but weren’t satisfied.

5.  Inactive Members Are More Likely to Leave 
   -  Active members (using their accounts frequently) have lower churn rates. 
   - Encouraging engagement may help reduce churn.

## Model Training & Performance
We trained  three models :
1.  Logistic Regression :
   - Accuracy: ~80%
   - Works well but struggles with complex relationships.
2.  Random Forest (Best Model!) :
   - Accuracy: ~86%
   - Shows best performance and feature importance ranking.
3.  Neural Network :
   - Accuracy: ~84%
   - Slightly worse than Random Forest, but good for complex patterns.

## Feature Importance (Random Forest)
1.  Age  - 24% (Most important!)
2.  Estimated Salary  - 14%
3.  Credit Score  - 14%
4.  Balance  - 14%
5.  NumOfProducts  - 13%
6.  Tenure  - 8%

Prediction Example:
A  35-year-old male from Germany with a credit score of 700 and a balance of 120,000  is  likely to stay .

Next Steps:
- Improve feature engineering (add more behavioral data).
- Try advanced models (XGBoost, Deep Learning).
- Optimize hyperparameters for better accuracy.
- Develop a real-world deployment strategy for banks.

🚀  Conclusion: 
This project successfully identified key factors affecting customer churn and built a predictive model to help banks retain their customers! 🎉

