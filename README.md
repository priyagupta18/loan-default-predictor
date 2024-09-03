
The dataset for this project can be accessed using the following link:

- **[Data Link (Train and Test)](https://drive.google.com/drive/folders/1xY5bzHJ5Pw9xcfGbQsRXlO41fqjhzmLX?usp=drive_link)**

## File Structure Overview -
- `eda_featureengg.ipynb` - This is the starting point. Here I have loaded and cleaned the data. EDA is also perfomed and feature generation has been done. The final dataset is saved. It can be found in the drive - data/train/final_df.csv
- `eda2_finalcleaning.ipynb` - Loaded the dataset generated using the above notebook. EDA is done and some minor feature engineering and outlier handling. The final dataset is saved. It can be found in the drive - data/train/final_df_outlier.csv 
- `model_building.ipynb` - This is where the model building takes place. Model pipeline is saved as voting_clf_pipeline.pkl
- `prediction_part/test_featureengg.ipynb` - Test dataset is generated using the same process as used in train dataset generation
- `prediction_part/test_prediction.ipynb` - Here predictions are generated using the voting_clf_pipeline.pkl model

## Generated Columns

The dataset includes the following generated columns:

- **`uid`**: Unique identifier for each record.
- **`applied_contract_type`**: Type of contract applied for by the user.
- **`target`**: Binary target variable indicating the outcome of interest.
- **`total_tl`**: Total number of loans held by the user.
- **`complete_tl`**: Number of loans completed by the user.
- **`active_tl`**: Number of active loans currently held by the user.
- **`amount_overdue_sum`**: Total amount overdue across all loans.
- **`loan_amount_avg`**: Average loan amount.
- **`loan_amount_min`**: Minimum loan amount.
- **`loan_amount_max`**: Maximum loan amount.
- **`num_times_delinquent`**: Number of times the user has been delinquent.
- **`months_since_recent_delinquency`**: Number of months since the most recent delinquency.
- **`automobile_loans`**: Number of automobile loans.
- **`business_loans`**: Number of business loans.
- **`consumer_loans`**: Number of consumer loans.
- **`mortgages_and_real_estate_loans`**: Number of mortgages and real estate loans.
- **`other_loans`**: Number of other types of loans.
- **`enquiry_count`**: Total number of inquiries made.
- **`max_enquiry_amount`**: Maximum amount inquired.
- **`time_since_last_enquiry`**: Number of months since the last inquiry.
- **`business_loans_enquiries`**: Number of inquiries related to business loans.
- **`consumer_loans_enquiries`**: Number of inquiries related to consumer loans.
- **`revolving_loans_enquiries`**: Number of inquiries related to revolving loans.
- **`mortgages_and_real_estate_loans_enquiries`**: Number of inquiries related to mortgages and real estate loans.
- **`other_loans_enquiries`**: Number of inquiries related to other types of loans.
- **`automobile_loans_enquiries`**: Number of inquiries related to automobile loans.

## Steps Performed

- **Loaded Data**: Data was loaded after proper formatting to ensure it was ready for preprocessing and analysis.
- **Data Cleaning**: Removed duplicates and addressed messy data to ensure quality and consistency in the dataset.
- **Generated New Columns**: Created additional features to enhance the model's predictive power.
- **Exploratory Data Analysis (EDA)**: Analyzed data distributions, correlations, and patterns to gain insights and understand the data better.
- **Outlier Handling**: Identified and managed outliers to reduce their impact on model performance.
- **Feature Selection**: Selected 16 features from the original 24 features to improve model performance and reduce complexity.
- **Encoding**: Applied encoding techniques to convert categorical variables into numerical format suitable for modeling.
- **Log Transformation**: Applied log transformation to skewed variables to normalize their distributions.
- **Standardization**: Standardized numerical features to bring them to a common scale.
- **Data Imbalance Handling**: Used SMOTE (Synthetic Minority Over-sampling Technique) and undersampling to address class imbalance.
- **Modeling**: Built and tuned machine learning models with hyperparameter optimization to achieve the best performance.

## Model Pipeline

The final model pipeline includes data preprocessing, class balancing, and a Voting Classifier combining LightGBM, XGBoost, and RandomForest. The pipeline is saved for future use.
