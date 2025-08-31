# Car Price Prediction ML Project

This project uses machine learning (scikit-learn) to predict car prices based on various features from a dataset (`car data.csv`). The workflow covers data preprocessing, modeling, evaluation, and prediction for new data.

## Features

- Uses Random Forest Regression for accurate price prediction.
- Preprocessing pipeline for categorical and numerical features.
- Train/test split for reliable evaluation.
- Model saving and loading for reuse.
- Example prediction for new car data.

## Dataset

The dataset (`car data.csv`) should be placed in the root directory, and has the following columns:

- **Car_Name**: Name of the car (not used for prediction)
- **Year**: Manufacturing year
- **Selling_Price**: Price for which the car is being sold (target variable)
- **Present_Price**: Current ex-showroom price
- **Driven_kms**: Kilometers driven
- **Fuel_Type**: Type of fuel (Petrol, Diesel, CNG)
- **Selling_type**: Dealer or Individual
- **Transmission**: Manual or Automatic
- **Owner**: Number of owners

## How to Run

1. **Clone the repository** and place `car data.csv` in the root directory.
2. Use either the provided Python script or Jupyter Notebook:
   - `car_price_prediction.py`
   - `car_price_prediction.ipynb`
3. Install required dependencies:

    ```bash
    pip install pandas numpy scikit-learn joblib
    ```

4. **Run the notebook or script:**  
   - For Jupyter Notebook:

        ```bash
        jupyter notebook car_price_prediction.ipynb
        ```

   - For Python script:

        ```bash
        python car_price_prediction.py
        ```

5. The model will print R² and RMSE scores, and save itself as `car_price_model.pkl`.

## Example Prediction

To predict the selling price of a new car, use the following format:

```python
new_car = {
    'Year': 2018,
    'Present_Price': 9.83,
    'Driven_kms': 2071,
    'Fuel_Type': 'Diesel',
    'Selling_type': 'Dealer',
    'Transmission': 'Manual',
    'Owner': 0
}
predicted_price = predict_price(new_car)
print("Predicted Selling Price:", predicted_price)
```

## Project Structure

```
car data.csv
car_price_prediction.py
car_price_prediction.ipynb
README.md
```

## License

This project is for educational purposes.

---

**Author:** [SamrahFar](https://github.com/SamrahFar)
