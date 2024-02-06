# Bitcoin Price Prediction using Linear Regression

## Overview
This project focuses on predicting Bitcoin prices using linear regression. It employs historical Bitcoin price and hash rate data to forecast future prices. The analysis includes feature engineering, moving average calculations, and model evaluation using mean squared error (MSE) for different prediction horizons.

## Data Source
The data is sourced from a file named 'BTC_Hash_2024-01-17.xlsx' containing Bitcoin prices and hash rates from 2009-01-09 to 2024-01-17.

## Key Steps
1. **Data Loading**: Load the data using Pandas.
2. **Feature Engineering**: Convert date strings to datetime objects and set them as the DataFrame index.
3. **Price Prediction**: Shift Bitcoin prices to create columns for different prediction horizons (1 to 30 days ahead).
4. **Hash Rate Moving Averages**: Calculate moving averages of hash rates for varying windows (1 to 30 days).
5. **Data Cleaning**: Drop rows with NaN values resulting from shifts and rolling means.
6. **Feature Selection**: Select hash rate moving averages and current Bitcoin price as features.
7. **Model Training and Testing**: Split data into training and testing sets. Train a linear regression model and evaluate its performance using MSE.

## Model Evaluation
- **MSE Analysis**: Plot MSE for training and testing data across different horizons and feature counts.
- **Optimal Feature Selection**: Determine the optimal moving average period for prediction based on MSE.
- **Final Model Training**: Train the model using the selected features and predict Bitcoin prices.

## Visualization
- **MSE Trends**: Visualize the MSE for training and testing datasets for various prediction horizons and feature counts.
- **Price Prediction**: Plot the actual and predicted Bitcoin prices for a selected period.
- **Hash Rate vs Price Scatter Plot**: Visualize the relationship between Bitcoin hash rate and price.

## Usage
To use this project:
1. Ensure you have Python installed with the necessary libraries: pandas, sklearn, matplotlib, and numpy.
2. Download the 'BTC_Hash_2024-01-17.xlsx' file containing the required data.
3. Run the provided Python script to perform the analysis and generate predictions.

## Dependencies
- pandas
- sklearn
- matplotlib
- numpy

## Contributing
Contributions, issues, and feature requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)

---

*This README is a guide to the Bitcoin price prediction project using linear regression. It outlines the steps taken in the analysis, model training, evaluation, and the necessary prerequisites for running the project.*
