# Telecom Data Churn Analysis

   In this project, the goal is to identify churn customers, that is, customers most likely to cancel subscription to a fictitious telecom company. Customer churn is a really interesting problem, because once identified, it is possible to focus on retention actions, providing adequate intervention to encourage them to stay and minimize customer exit. The dataset for this project was obtained from the [OpenML](https://www.openml.org/d/40701) public repository. The dataset relating features of account and usage for churn and non churn clients. In the context of this project, this is a problem of supervised classification and Machine Learning algorithms will be used for the development of predictive models and evaluation of accuracy and performance. It seeks to find the most appropriate model for the business.

# 1. Churn

  Churn Customer can be defined as a user who is likely to discontinue using the services. So, the target variable confirm if the customer has churned (1=yes; 0 = no).

# 2. Dataset

   The data included 5.000 users and by the exploratory analysis, it is observed that:

   * 14% of the base are classified as churn.
   * 50% of the customers who called the company more than 3 times are classified as Churn.
   * 10% of those with no international plan are classified as Churn x 8% of those with an international plan are Churn.
   
  ### 2.1 Columns
   
   * ID 
   
      * 'area_code'
      * 'phone_number'


   * Features 
   
      * 'state'
      * 'account_length'
      * 'international_plan'
      * 'voice_mail_plan'
      * 'number_vmail_messages'    
      * 'total_day_minutes'
      * 'total_day_calls'
      * 'total_day_charge'
      * 'total_eve_minutes' 
      * 'total_eve_calls'
      * 'total_eve_charge'
      * 'total_night_minutes'
      * 'total_night_calls'
      * 'total_night_charge'
      * 'total_intl_minutes'
      * 'total_intl_calls'
      * 'total_intl_charge'
      * 'number_customer_service_calls'

   * Target
   
      * 'class'
      
 # 3. Features Importance

   Feature selection process of finding and selecting the most useful features in a dataset. Unnecessary features decrease training speed, the model interpretability and the generalization performance on the test set. Estimating the influence of a given feature to a model prediction is importante mainly in large datasets for performance gain by selecting only the most relevant ones.
   
   According to the feature importance analysis produced by the Random Forest algorithm, the following features had the highest predictive power:

    1. total_day_minutes
    2. total_day_charge
    3. number_customer_service_calls
    4. total_eve_minutes
    5. international_plan     
       	     
    
#  4. Modeling and Results
   
   The 18 characteristics of this data set were used to train the models.

Their respective AUC (Area Under the Curve) measures are listed below:
    
    Gradient Boosted Trees: 0.92
    Random Forest:    0.91
    AdaBoost: 0.87
    Logistic Regression: 0.82

Gradient Boosted Classifier produced the highest AUC and the following scores:

      Accuracy: 96% labeled correctly
      Precision: 93% labeled as churn actually churned (5% were wrongly labeled as churn)
      Recall: 74% that actually churned were labeled as churn (2% of churn users were labeled as non-churn)
   
   The best results achieved by the [OpenML](https://www.openml.org/t/167141) users for this dataset have had results similar to this one, 95% accuracy using Random Forest. However, in this project, we were able to optimize this result using Gradient Boosted Classifier, with 96% accuracy.   

# 6. Tools
    Jupyter notebook, Python (Sklearn, Pandas, Numpy, Matplotlib and Seaborn)

   Code: [link](https://github.com/thaiseq/Analytics/blob/master/Telecom%20Data%20Churn%20Analysis.ipynb)
   
   


    
