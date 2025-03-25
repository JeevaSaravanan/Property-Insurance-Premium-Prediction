

# Property Insurance Premium Pricing Optimization

## Aim of the Project
To develop a machine learning model that accurately predicts property insurance premiums based on property characteristics and risk factors.

## Overview
This project uses data analytics and machine learning to analyze property insurance data, extract meaningful insights, and predict insurance premiums. The process encompasses data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and evaluation, with the goal of informing business strategies for premium pricing.

## Objectives
- **Predictive Modeling:** Develop a robust model to estimate insurance premiums.
- **Insight Discovery:** Identify key drivers impacting premium prices.
- **Business Optimization:** Provide actionable recommendations to optimize insurance premium strategies.
- **Data Understanding:** Enhance the understanding of property and risk-related factors in premium determination.

## Dataset Description
The dataset comprises various features related to property details, risk assessments, and historical premium data. For a detailed description of each feature, please refer to the [Dataset Features.txt](Dataset%20Features.txt) file. Key aspects include:

- **Property Characteristics:**  
   - **PROPERTY_TYPE, YEAR_OF_CONSTRUCTION, PROPERTY_LOCATION, PROPERTY_AREA** physical and locational attributes of the property.

- **Risk Factors:**  
   - **HAZARD_EXPOSURE, SAFETY_FEATURES** likelihood or severity of potential insurance claims due to various risks.

-  **Financial Metrics:**  
   - **ANNUAL_PREMIUM, PROPERTY_VALUATION, HISTORICAL_CLAIMS**  it relates directly to monetary considerations

-  **Demographic/Temporal Columns:**  
   - **GENDER, AGE, QUOTE_MONTH, COVER_START_MONTH** policyholder demographics and timings 

-  **General Columns:**  
   - **POLICY_ID**  unique id for a policy.


## Methodology
The project methodology follows a systematic pipeline:

1. **Data Preprocessing:**
   - Cleaning the data by addressing missing values and outliers.
   - Normalizing and scaling features to prepare for model training.
2. **Feature Engineering:**
   - Creating new features from existing data.
   - Selecting and transforming features to enhance model performance.

### Exploratory Data Analysis (EDA)


![alt text](</images/num_of_building_vs_year.png>)

- **Significant Peaks:** There are notable spikes in the number of buildings around the early 1900s and a very prominent peak around the 1950s. This may indicate periods of construction booms or post-war housing expansions.
- **Decline in Late 20th Century:** After the 1950s peak, there is a downward trend, suggesting fewer buildings for later construction years.
 
- **Feature Engineering:** Created a new feature **Property Age** (`Current Year - Year of Construction`)



![alt text](</images/dist_quote_month_&_cover_start_month.png>)


* **Seasonal Peaks:** Both **QUOTE_MONTH** and **COVER_START_MONTH** show higher frequencies in the January–February and the October–December. This indicates seasonality or cyclical behavior in how customers request quotes and when coverage actually begins.

* **Potential Business/Policy Cycles:** : Companies or customers might prefer to initiate coverage in January for alignment with fiscal years or personal budgeting cycles, leading to higher activity in early months.

* **Actionable Insights:**  :
  -  **Staffing & Marketing:** Insurance companies may need to allocate more resources during peak months to handle increased quote requests and policy starts.  
  - **Pricing & Promotions:** Promotional or targeted marketing strategies could be timed to address mid-year lulls and capture additional business outside 
  peak months.

![alt text](</images/dist_payment_method.png>) ![alt text](</images/dist_gender.png>)



![alt text](</images/joint_plot_age_vs_premium.png>)

**Minimal Direct Correlation:** The scatter plot reveals no strong linear relationship between a policyholder’s age and their annual premium, indicating that other factors likely drive premium pricing.
**Predominantly Moderate Premiums:** Most data points cluster around lower premium values (under 1,500), suggesting that high premiums are outliers rather than the norm.

![alt text](</images/box_plot_bedroom_listed.png>)

- **Bedroom Count & Property Age**  
   - Properties with fewer bedrooms exhibit a wide range of construction years, suggesting they include both older and newer buildings.  
   - Larger-bedroom properties appear more consistent in construction era, potentially reflecting modern building standards or expansions in specific time periods.

- **Listed Properties**  
   - Certain listed categories correspond to older construction years, indicating historical or heritage status.  
   - More recent listings may point to properties updated or newly registered, reflecting ongoing changes in real estate classification and preservation efforts.


## Results & Insights
- **Model Performance:** The final model achieved competitive performance as measured by metrics such as RMSE, MAE, and R².
- **Key Drivers:** Analysis revealed that factors like property location, construction type, and risk indicators are significant predictors of insurance premiums.
- **Business Insights:** The findings provide valuable guidance for premium pricing strategies and risk assessment processes.

## Business Action Plan
Based on the project findings, the following actions are recommended:
- **Enhanced Risk Assessment:** Utilize the model's insights to refine risk evaluation protocols.
- **Premium Adjustment:** Tailor premium pricing to more accurately reflect individual property risk profiles.
- **Product Development:** Consider developing specialized insurance products for properties with distinct risk features.
- **Data-Driven Strategy:** Integrate predictive analytics into underwriting and policy decision processes to improve overall business outcomes.


## Technologies Used

- **Python** (Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib)
- **Machine Learning Models**: Logistic Regression, Random Forest, SVM, KNN, Decision Tree, Gradient Boosting, XGBoost, LightGBM, CatBoost
<!-- - **SHAP** for explainability and feature importance.
-->

## Project Structure

```
project-root/
│
├── data/
|   ├──insurance.csv
│   └──home_insurance_dataset.csv
│
├── notebooks/
│   └── property_insurance_premium_prediction.ipynb
│
├── Images/
│   └── 
│
└── README.md
```

<div align="center">

<a href="https://jeevasaravanan.medium.com/" target="_blank">![Medium](https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white)</a> <a href="https://www.linkedin.com/in/jeeva-saravanan/" target="_blank">![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)</a> <a href="https://jeeva-saravana-bhavanandam.web.app" target="_blank">![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=GoogleChrome&logoColor=white)</a>


</div>

