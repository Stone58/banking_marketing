# Bank Marketing Dataset Analysis: 

## Overview

This repository contains ETL process, exploratory data analysis (EDA) and predictive modeling on the Bank Marketing dataset using PySpark. 
The analysis aims to understand patterns in customer behavior and predict marketing outcomes for a bank. [Link available in here](https://archive.ics.uci.edu/dataset/222/bank+marketing)
Below is the workflow used : 

![Workflow](https://github.com/Stone58/banking_marketing/blob/main/plots/banking_diagram.png)

## Tools and Technologies Used

- **PySpark:** Utilized for scalable data processing, ETL operations, and machine learning model training.
- **Jupyter Notebook:** Interactive environment used for code development, data visualization, and documentation.
- **Pandas:** : for data transformation and ploting purposes
- **Matplotlib and Seaborn:** Python libraries for creating visualizations to explore data distributions, correlations, and trends.

## Dataset Description

The Bank Marketing dataset consists of data related to direct marketing campaigns of a Portuguese banking institution. The dataset contains both categorical and numerical features, providing insights into customer demographics, campaign details, and outcomes.


### Features in the Dataset

- **Categorical Features:**
  - `job`: Type of job (e.g., admin, blue-collar, technician)
  - `marital`: Marital status (e.g., married, single)
  - `education`: Education level (e.g., primary, secondary, tertiary)
  - `default`: Whether the customer has credit in default (yes/no)
  - `housing`: Whether the customer has a housing loan (yes/no)
  - `loan`: Whether the customer has a personal loan (yes/no)
  - `contact`: Communication type during the campaign (e.g., cellular, telephone)
  - `month`: Last contact month of the year (e.g., jan, feb)
  - `day_of_week`: Last contact day of the week (e.g., mon, fri)
  - `poutcome`: Outcome of the previous marketing campaign (e.g., success, failure)

- **Numerical Features:**
  - `age`: Age of the customer
  - `duration`: Duration of the last contact in seconds
  - `campaign`: Number of contacts performed during this campaign for this client
  - `previous`: Number of contacts performed before this campaign for this client
  - `emp_var_rate`: Employment variation rate (quarterly indicator)
  - `cons_price_idx`: Consumer price index (monthly indicator)
  - `cons_conf_idx`: Consumer confidence index (monthly indicator)
  - `euribor3m`: Euribor 3-month rate (daily indicator)
  - `nr_employed`: Number of employees (quarterly indicator)

## Goal of Analysis

The primary goal of this analysis is twofold:

1. **Exploratory Data Analysis (EDA) after ETL of important features and informations:**
   - Perform exploratory data analysis to understand the distribution, relationships, and trends within the dataset.
   - Visualize key features and their impact on marketing outcomes using plots and statistical summaries.
   - Identify patterns in customer behavior, such as preferred communication channels, response rates to campaigns, and demographic influences.

2. **Predictive Modeling:**
   - Build predictive models to forecast whether a customer will subscribe to a term deposit (binary classification).
   - Evaluate model performance using metrics such as accuracy, precision, recall, and ROC-AUC.
   - Utilize PySpark's capabilities for data preprocessing, feature engineering, and model training to demonstrate proficiency in scalable data processing and analysis.

## Results : 

  ### EDA Results: From the data, we could observe that:
  ![Ploting of calling days ](https://github.com/Stone58/banking_marketing/blob/main/plots/marketing_call_days.png)
  ![Plot showing job status of the consumers ](https://github.com/Stone58/banking_marketing/blob/main/plots/job_status_of_consumer_called.png)
  ![Ploting showing the loan status of the consumers ](https://github.com/Stone58/banking_marketing/blob/main/plots/consumer_and_their_loan_status.png)
  ![Age distribution of the consumers ](https://github.com/Stone58/banking_marketing/blob/main/plots/age%20distribution%20of%20the%20called%20consumers.png)
  
  - **Age Distribution:** People between 30-40 years old were the most called.
  - **Average Contact Duration:** Most marketing-goal contacts lasted for roughly 250 seconds.
  - **Frequency of Contact:** During marketing, clients were typically contacted once.
  - **Time Since Last Campaign:** Most clients were contacted almost 3 years after a previous campaign.
  - **Outcome of Last Campaign:** The majority of clients were not contacted during the last campaign, with only a few (almost 5000 persons) contacted once.
  - **nr_employed:** More than 16,000 instances have `nr_employed` values greater than 5,200, suggesting a significant portion of the dataset reflects periods with relatively higher levels of employment, which is also explained by `emp_var_rate`.
  - **Consumer Behavior:** As shown by the barplot, consumers tend to be optimistic and spend more, possibly leading to increased spending.
  - **cons_price_idx:** The higher value of `cons_price_idx` indicates inflationary pressure and an increase in consumer prices.
  - **euribor3m:** `euribor3m`, which represents the average interest rate at which European banks lend to each other for a three-month period, shows relative stability.

  - **job:** Most of the consumers involved in the research were admins, with few being students or unemployed.
  - **marital:** The majority of consumers were married.
  - **education:** Most of the users called had a university degree or high school diploma.
  - **default:** The consumers called didn't have personal credit defaults.
  - **housing:** Most of the consumers called were on a housing loan.
  - **loan:** The majority of the consumers called did not have any personal loans.
  - **contact:** Most calls were directed towards cellular users.
  - **month:** Most marketing efforts occurred in May, possibly due to events like Mother's Day or regular work days.
  - **day_of_week:** The most marketing calls happened on Mondays and Thursdays.
  - **poutcome:** Although most customers weren't contacted before (86%), there were more failures in attempts than successes.

### Machine Learning results : 
  - Through feature importance we can see that **the duration** of the call is the factor that influence the marketing output the most , which is understandable because a customer interested would be asking more details about the campain than someone not interested. 
  - Due to the imbanlance form of the dataset, f1 metric was used to evaluate the dataset and a score of **89,98%** was obtained on the dataset using Linear regression algorithm. This result suggests that the features selected for the analysis can be used to predict the sucess of a marketing call.
  - Also, an accuracy of **92,91%** was obtained.
    
## Conclusion
This repository showcases an end-to-end analysis of the Bank Marketing dataset, highlighting exploratory data analysis techniques, predictive modeling, and the use of PySpark for scalable data processing. 
The insights gained from this analysis can inform marketing strategies aimed at improving campaign effectiveness and maximizing customer engagement.

## Future updates : 
  - The dataset is imbanlanced, undersampling techniques could be used 

