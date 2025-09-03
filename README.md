# House-Price-Prediction
House Price Prediction & City Quality Analysis
This project explores house price prediction by combining the classic Boston housing dataset with additional city quality-of-life indices sourced via web scraping. It demonstrates an end-to-end workflow including data collection, cleaning, feature engineering, model building, and evaluation in Python.

Features
Data Sources:

Boston Housing Dataset (from scikit-learn/openml)

US City Quality of Life indices (scraped from Numbeo)

Main Steps:

Load and inspect the Boston housing dataset.

Scrape and parse city-level indices (e.g., Quality of Life, Purchasing Power, Safety, Health, Climate) using requests & BeautifulSoup.

Merge housing and city datasets using synthetic ZIP codes for demonstration.

Data cleaning: handle nulls, duplicates, and outliers (custom IQR-based function).

Exploratory Data Analysis (EDA): summary statistics, feature visualization.

Model Building:

Linear Regression

Random Forest Regressor

XGBoost Regressor

Pipelines for preprocessing, scaling, encoding, and imputation.

Evaluation: Mean Squared Error, R² score, and visualization of predictions.

Notable Code Sections
Web Scraping and Parsing:

Extracted HTML tables with city indices from Numbeo.

Converted scraped text data to numeric formats for analysis.

Data Integration:

Merged datasets on ZIP code to enrich each house record with its city’s quality metrics.

Machine Learning Models:

Used scikit-learn and XGBoost to train and evaluate different regression models for price prediction.

Requirements
Python 3.8+

pandas, numpy, scikit-learn, xgboost, requests, beautifulsoup4, matplotlib, seaborn

How to Run
Clone the repository.

Run house_price_prediction.ipynb in Jupyter Notebook or compatible environment.

Ensure all dependencies are installed (see Requirements).

Follow code cells for stepwise execution from data import to model evaluation.

Potential Warnings/Errors
Boston dataset may prompt deprecation or multi-version warnings.

Numbeo scraping may fail if site structure changes.

Numeric conversion or merging may cause ValueErrors if the scraped data has inconsistencies.

Machine learning code may raise DataConversion or shape mismatch warnings if input data is not cleaned.

Results
Predicts house prices using both traditional housing features and city-level indices.

Evaluates multiple regression approaches and compares performance metrics.

Visualizes relationships between urban quality metrics and housing costs.

License
MIT License.

Author: Suryansh Singh Solanki
