# Credit Risk Modelling Classification

This project is a credit risk modeling application that predicts the probability of default, credit score, and rating for loan applicants. It uses machine learning techniques and a pre-trained model to perform these predictions.

## Project Structure

- **main.py**: A Streamlit-based web application that provides a user interface for inputting loan applicant details and displaying predictions.
- **prediction_helper.py**: Contains helper functions for preparing input data, making predictions, and calculating credit scores.
- **artifacts/model_data.joblib**: A serialized file containing the pre-trained model, feature list, scaler, and columns to scale.
- **requirements.txt**: Lists the Python dependencies required for the project.

## Steps Performed

1. **Data Preparation**:
   - User inputs are collected via the Streamlit interface in `main.py`.
   - The `prepare_input` function in `prediction_helper.py` processes these inputs, ensuring all required features are present and scaled appropriately.

2. **Prediction**:
   - The `predict` function in `prediction_helper.py` uses the pre-trained model to calculate the default probability, credit score, and rating.

3. **Credit Score Calculation**:
   - The `calculate_credit_score` function applies a logistic function to compute the default probability and converts it into a credit score scaled between 300 and 900.
   - A rating is assigned based on the credit score.

4. **Results Display**:
   - The predictions are displayed on the Streamlit interface, including default probability, credit score, and rating.

## Tools and Libraries Used

- **Streamlit**: For building the web application interface.
- **Joblib**: For loading the pre-trained model and its components.
- **NumPy**: For numerical computations.
- **Pandas**: For data manipulation and preparation.
- **scikit-learn**: For scaling input features using `MinMaxScaler`.

## How to Run the Application

1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the Streamlit application:
   ```bash
   streamlit run main.py
   ```

3. Open the provided URL in your browser to access the application.

## Notes

- Ensure the `artifacts/model_data.joblib` file is present in the correct directory.
- The application assumes the pre-trained model is compatible with the input features and scaling logic defined in `prediction_helper.py`.

## Future Enhancements

- Add support for additional loan purposes and residence types.
- Improve the user interface for better usability.
- Incorporate more advanced machine learning models for better predictions.