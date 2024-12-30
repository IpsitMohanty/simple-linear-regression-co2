# Simple Linear Regression for Predicting CO2 Emissions

## Project Overview
This project demonstrates how to use **Simple Linear Regression** to predict **CO2 emissions** of vehicles based on features such as **engine size** and **fuel consumption**. By analyzing this dataset, we aim to:

- Understand the relationship between vehicle features and CO2 emissions.
- Build a regression model to make predictions.
- Evaluate the model's performance and identify key factors affecting emissions.

## Dataset Description
The dataset used in this project contains model-specific fuel consumption ratings and estimated CO2 emissions for light-duty vehicles. It provides real-world data sourced from Canadian vehicle statistics.

### Key Columns in the Dataset
- **MODELYEAR**: The year of manufacture.
- **MAKE**: Vehicle manufacturer.
- **MODEL**: Vehicle model.
- **VEHICLE CLASS**: Classification of the vehicle (e.g., SUV, sedan).
- **ENGINE SIZE**: Engine size in liters.
- **CYLINDERS**: Number of cylinders in the engine.
- **FUELCONSUMPTION_CITY**: Fuel consumption in the city (L/100 km).
- **FUELCONSUMPTION_HWY**: Fuel consumption on the highway (L/100 km).
- **FUELCONSUMPTION_COMB**: Combined fuel consumption (L/100 km).
- **CO2EMISSIONS**: Carbon dioxide emissions in grams per kilometer (target variable).

## Objectives
1. Predict **CO2 emissions** based on:
   - `ENGINESIZE` (Simple Linear Regression Model 1).
   - `FUELCONSUMPTION_COMB` (Simple Linear Regression Model 2).
2. Evaluate and compare the models using metrics such as:
   - **Mean Absolute Error (MAE)**
   - **Mean Squared Error (MSE)**
   - **R-squared (R²)**

## Key Steps

### 1. Data Loading and Exploration
- Load the dataset and inspect its structure.
- Visualize relationships between features (e.g., scatter plots for `ENGINESIZE` vs `CO2EMISSIONS`).

### 2. Feature Selection
- Focused on two features for simplicity:
  - `ENGINESIZE`
  - `FUELCONSUMPTION_COMB`

### 3. Data Splitting
- Split the data into:
  - **Training Set (80%)**: Used to train the regression models.
  - **Testing Set (20%)**: Used to evaluate the model's performance.

### 4. Model Training
- Trained two Simple Linear Regression models:
  - Model 1: Predict CO2 emissions using `ENGINESIZE`.
  - Model 2: Predict CO2 emissions using `FUELCONSUMPTION_COMB`.

### 5. Model Evaluation
- Evaluated the models using:
  - **MAE**: Average magnitude of prediction errors.
  - **MSE**: Penalizes larger errors more heavily.
  - **R²**: Proportion of variance explained by the model.

### 6. Comparison of Models
- Found that `FUELCONSUMPTION_COMB` is a better predictor than `ENGINESIZE`.

## Key Results

| Feature Used           | MAE   | MSE     | R²   |
|------------------------|-------|---------|-------|
| `ENGINESIZE`           | 132.68| 20000   | 0.50  |
| `FUELCONSUMPTION_COMB` | 19.26 | 987.85  | 0.75  |

### Insights
- `FUELCONSUMPTION_COMB` has a stronger and more direct correlation with CO2 emissions compared to `ENGINESIZE`.
- Adding more features like `CYLINDERS` or `FUELCONSUMPTION_CITY` might further improve predictions.

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/IpsitMohanty/simple-linear-regression-co2.git
   cd simple-linear-regression-co2

   ## How to Run the Project

### Install Dependencies
To set up the environment, install the required Python libraries:

```bash
pip install pandas matplotlib scikit-learn
```

### Run the Notebook
1. Open `ML0101EN_Reg_Simple_Linear_Regression_Co2_v2.ipynb` in Jupyter Notebook or Google Colab.
2. Execute the cells step by step to:
   - Train the regression models.
   - Visualize the results.
   - Evaluate model performance.

## Future Work
- **Feature Expansion**: Include additional features such as `CYLINDERS` and `TRANSMISSION` to build a multivariate regression model.
- **Non-Linear Models**: Explore more advanced algorithms like polynomial regression or tree-based models.
- **Outlier Analysis**: Evaluate and mitigate the impact of outliers on predictions for improved accuracy.


## Acknowledgments
- **Dataset Source**: Sourced from Canadian vehicle statistics.
- **Purpose**: Developed as part of a learning exercise in Machine Learning.

