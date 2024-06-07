# Vehicle Sales Price Prediction

This project focuses on predicting vehicle selling prices using various machine learning models. The dataset used for this project is sourced from [Kaggle](https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data/data).

## Project Overview

The main objective of this project is to build and evaluate machine learning models to predict the selling prices of vehicles based on various features. The project includes:

1. Data Preprocessing and Cleaning
2. Feature Engineering
3. Model Training and Evaluation
4. Incorporating Regularization
5. Using Ensemble Methods
6. Hyperparameter Tuning

## Dataset

The dataset used in this project contains information about vehicle sales, including various attributes like vehicle make, model, year, odometer reading, condition, and selling price. The dataset can be found on Kaggle:

[Vehicle Sales Data](https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data/data)

### Data Preprocessing

The dataset was preprocessed to handle missing values, encode categorical variables, and create new features. This preprocessing step ensures that the data is in the right format for training machine learning models.

### Feature Engineering

Several new features were engineered to improve the model's performance, including:
- Vehicle Age
- Log-transformed Odometer
- Interaction terms between features

### Models Used

The following machine learning models were trained and evaluated:
- Linear Regression
- Random Forest
- Gradient Boosting
- XGBoost
- Stacking Ensemble

### Regularization

Regularization techniques, including L1 (Lasso) and L2 (Ridge), were incorporated to prevent overfitting and improve model generalization. However, it was observed that incorporating regularization worsened the results for this specific dataset and model configuration.

### Evaluation Metrics

The models were evaluated using the following metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R-squared (R²)

### Cross-Validation

Cross-validation was used to ensure the robustness and generalization of the models. The models were evaluated using 5-fold cross-validation.

### Final Model

The final model is a stacking ensemble that combines predictions from Random Forest, Gradient Boosting, and XGBoost models with a Linear Regression meta-model. This model achieved the best performance without explicit regularization.

## Results

The final stacking ensemble model without explicit regularization achieved the following results:

- **Stacking Ensemble MAE**: 1527.13
- **Stacking Ensemble MSE**: 6,218,317.14
- **Stacking Ensemble R-squared**: 0.9281
- **Cross-Validation MAE**: 1525.47 (± 74.30)
- **Cross-Validation MSE**: 5,762,890.72 (± 911,057.79)
- **Cross-Validation R-squared**: 0.9326 (± 0.0025)

### Comparison with Regularization

When incorporating regularization, the model's performance metrics worsened:
- **MAE with Regularization**: 1934.46
- **MSE with Regularization**: 8,910,290.73
- **R-squared with Regularization**: 0.8970
- **Cross-Validation MAE with Regularization**: 1905.63 (± 69.73)
- **Cross-Validation MSE with Regularization**: 8,442,678.54 (± 1,357,772.91)
- **Cross-Validation R-squared with Regularization**: 0.9012 (± 0.0044)

This indicates that regularization, while generally helpful for preventing overfitting, was not beneficial for this particular dataset and model configuration.

## Installation

To run this project, you need to have Python and the required libraries installed. You can install the dependencies using the following command:

```bash
pip install -r requirements.txt
```

## Usage

To use the code in this repository, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/TaiNg365/vehicle-sales-price-prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd vehicle-sales-price-prediction
   ```
3. Run the Jupyter Notebook or Python scripts to preprocess the data, train the models, and evaluate their performance.

## Contributing

Contributions to this project are welcome. If you have any ideas, suggestions, or bug fixes, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgements

- [Kaggle](https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data/data) for providing the dataset.
- The authors of the libraries and tools used in this project.
