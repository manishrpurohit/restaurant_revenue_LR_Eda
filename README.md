# Restaurant Revenue Prediction - Linear Regression Analysis

## Project Overview
This project implements machine learning models to predict restaurant monthly revenue using supervised learning techniques. The analysis includes exploratory data analysis (EDA), data preprocessing, and comparison of multiple linear regression variants to identify the best-performing model.

## Dataset
- **Source**: Restaurant_revenue_dataset.xlsx
- **Target Variable**: Monthly_Revenue
- **Data Characteristics**:
  - Mixed data types (numerical and categorical features)
  - Duplicate entries removed
  - Missing values handled through mean imputation (numerical) and mode imputation (categorical)
  - Categorical features encoded using LabelEncoder

## Project Structure
```
restaurant_revenue_LR_Eda/
├── Restaurant Revenue.ipynb          # Main analysis notebook
├── Restaurant_revenue_dataset.xlsx    # Dataset file
└── README.md                          # Project documentation
```

## Methodology

### 1. Data Preprocessing
- Removed duplicate records
- Handled missing values:
  - Numerical columns: filled with mean values
  - Categorical columns: filled with mode values
- Encoded categorical variables using Label Encoding

### 2. Exploratory Data Analysis (EDA)
- Correlation analysis with heatmap visualization
- Feature relationships exploration
- Identified important predictors for revenue

### 3. Data Splitting
- Train-test split: 80-20 ratio
- Random state: 42 (for reproducibility)

### 4. Models Implemented
The project compares four linear regression models:

| Model | Configuration |
|-------|---------------|
| **Linear Regression** | Standard OLS |
| **Ridge Regression** | alpha = 1.0 |
| **Lasso Regression** | alpha = 0.1 |
| **ElasticNet Regression** | alpha = 0.1, l1_ratio = 0.5 |

### 5. Evaluation Metrics
- **MAE** (Mean Absolute Error): Average absolute prediction error
- **MSE** (Mean Squared Error): Squared error penalizing large deviations
- **RMSE** (Root Mean Squared Error): Scale-dependent error metric
- **R² Score**: Coefficient of determination (model fit quality)

## Key Outputs

### Model Performance Comparison
All four models are evaluated and compared using:
- Performance metrics (MAE, MSE, RMSE, R² Score)
- Feature importance coefficients
- Actual vs. Predicted scatter plots

### Feature Importance
- Features are ranked by their regression coefficients
- Identifies the most influential factors in revenue prediction

## Requirements

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
openpyxl  # For Excel file reading
```

## Installation

1. Clone the repository
2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Place the dataset file in the project directory

## Usage

1. Open `Restaurant Revenue.ipynb` in Jupyter Notebook or JupyterLab
2. Execute all cells sequentially
3. Review the model performance comparison
4. Identify the best-performing model for your use case

## Results & Insights

- **Best Model Selection**: Based on R² Score (highest value indicates best fit)
- **Feature Coefficients**: Shows the magnitude and direction of each feature's impact on revenue
- **Visualizations**: Scatter plots comparing actual vs. predicted values for each model

## Key Findings

The notebook generates:
- Correlation heatmap showing feature relationships
- Model performance metrics comparison table
- Feature importance rankings for each model
- Prediction accuracy visualizations

## Future Improvements

- Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
- Cross-validation for more robust performance estimates
- Polynomial features or interaction terms exploration
- Outlier detection and handling
- Feature scaling (StandardScaler/MinMaxScaler) evaluation
- Non-linear models comparison (Random Forest, Gradient Boosting)

## Author

Created as part of supervised machine learning projects

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to fork, improve, and submit pull requests!

## Contact

For questions or suggestions, please open an issue on GitHub.

---

**Note**: Update file paths in the notebook if running on a different system. The current implementation uses absolute paths that may need modification.
