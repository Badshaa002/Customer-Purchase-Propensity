# Summary Report

## Theory + Short Notes

- Data analysis is the process of collecting, cleaning, organizing, and studying data so that useful patterns and decisions can be made from it.
- A normal data science project follows these steps: understand the problem, collect data, clean and preprocess it, perform EDA, engineer features, transform the data, and prepare it for modeling.
- This project is framed as a binary classification problem because the target variable has only two classes: `purchased = 1` and `purchased = 0`.

## Observations

The project used four sources: `customers.csv`, `transactions.json`, `products.sql`, and a small `dummyjson` API sample stored as `api_users.json`. The files were merged using `customer_id` and `product_id`, then converted into a customer-level dataset. After merging, the final dataset contained 16 customer records with a balanced target distribution of 8 purchasers and 8 non-purchasers.

The biggest issues in the raw data were:
- the local customer data alone had only purchase records, so there was no `0` class for the target,
- income was missing for the API-added customers,
- transaction-related fields were missing for customers with no purchases,
- one transaction amount (`T007`) did not match the product catalog price.

The preprocessing techniques used were:
- median imputation for numeric columns,
- most-frequent imputation for categorical columns,
- missing indicator and random sample imputation,
- KNN imputation and MICE for comparison,
- Z-score, IQR, and percentile methods for outlier detection,
- label encoding, one-hot encoding, and ordinal encoding,
- StandardScaler, MinMaxScaler, MaxAbsScaler, RobustScaler, and Normalizer,
- feature engineering such as `days_since_signup`, `days_since_last_purchase`, `purchase_per_day`, income binning, and log transformation.

For this small dataset, `SimpleImputer` worked best as the final choice because it was stable and easy to explain. Among the scaling methods, `RobustScaler` was the most suitable because it handled extreme values better after outlier checks.
