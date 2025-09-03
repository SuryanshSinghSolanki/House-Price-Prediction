# House-Price-Prediction
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
</head>
<body>
  <h1>House Price Prediction & City Quality Analysis</h1>

  <p>
    This project explores <strong>house price prediction</strong> by combining the classic Boston housing dataset with additional <strong>city quality-of-life indices</strong> sourced via web scraping. It demonstrates an end-to-end workflow including data collection, cleaning, feature engineering, model building, and evaluation in Python.
  </p>

  <h2>Features</h2>
  <ul>
    <li><strong>Data Sources:</strong>
      <ul>
        <li>Boston Housing Dataset (from scikit-learn/openml)</li>
        <li>US City Quality of Life indices (scraped from Numbeo)</li>
      </ul>
    </li>
    <li><strong>Main Steps:</strong>
      <ul>
        <li>Load and inspect the Boston housing dataset.</li>
        <li>Scrape and parse city-level indices (e.g., Quality of Life, Purchasing Power, Safety, Health, Climate) using requests &amp; BeautifulSoup.</li>
        <li>Merge housing and city datasets using synthetic ZIP codes for demonstration.</li>
        <li>Data cleaning: handle nulls, duplicates, and outliers (custom IQR-based function).</li>
        <li>Exploratory Data Analysis (EDA): summary statistics, feature visualization.</li>
        <li>Model Building:
          <ul>
            <li>Linear Regression</li>
            <li>Random Forest Regressor</li>
            <li>XGBoost Regressor</li>
            <li>Pipelines for preprocessing, scaling, encoding, and imputation.</li>
          </ul>
        </li>
        <li>Evaluation: Mean Squared Error, R² score, and visualization of predictions.</li>
      </ul>
    </li>
  </ul>

  <h2>Notable Code Sections</h2>
  <ul>
    <li><strong>Web Scraping and Parsing:</strong>
      <ul>
        <li>Extracted HTML tables with city indices from Numbeo.</li>
        <li>Converted scraped text data to numeric formats for analysis.</li>
      </ul>
    </li>
    <li><strong>Data Integration:</strong>
      <ul>
        <li>Merged datasets on ZIP code to enrich each house record with its city’s quality metrics.</li>
      </ul>
    </li>
    <li><strong>Machine Learning Models:</strong>
      <ul>
        <li>Used scikit-learn and XGBoost to train and evaluate different regression models for price prediction.</li>
      </ul>
    </li>
  </ul>

  <h2>Requirements</h2>
  <ul>
    <li>Python 3.8+</li>
    <li>pandas, numpy, scikit-learn, xgboost, requests, beautifulsoup4, matplotlib, seaborn</li>
  </ul>

  <h2>How to Run</h2>
  <ol>
    <li>Clone the repository.</li>
    <li>Run <code>house_price_prediction.ipynb</code> in Jupyter Notebook or compatible environment.</li>
    <li>Ensure all dependencies are installed (see Requirements).</li>
    <li>Follow code cells for stepwise execution from data import to model evaluation.</li>
  </ol>

  <h2>Potential Warnings/Errors</h2>
  <ul>
    <li>Boston dataset may prompt deprecation or multi-version warnings.</li>
    <li>Numbeo scraping may fail if site structure changes.</li>
    <li>Numeric conversion or merging may cause ValueErrors if the scraped data has inconsistencies.</li>
    <li>Machine learning code may raise DataConversion or shape mismatch warnings if input data is not cleaned.</li>
  </ul>

  <h2>Results</h2>
  <ul>
    <li>Predicts house prices using both traditional housing features and city-level indices.</li>
    <li>Evaluates multiple regression approaches and compares performance metrics.</li>
    <li>Visualizes relationships between urban quality metrics and housing costs.</li>
  </ul>

  <h2>License</h2>
  <p>MIT License.</p>

  <hr>
  <p><strong>Author:</strong> Suryansh Singh Solanki</p>
</body>
</html>
