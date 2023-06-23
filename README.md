## Flask Car Price Prediction App

This is a Flask web application that predicts the selling price of a used car based on various input features. It uses a trained Random Forest Regression model to make the predictions.

## Usage
When you access the application, you will see a form where you can enter the details of the car.
Fill in the required fields, such as the year of the car, present price, kilometers driven, owner count, fuel type, seller type, and transmission type.
Click on the "Predict" button to submit the form.
The application will process the input and display the predicted selling price of the car.
## Description
The Flask Car Price Prediction App is built using the Flask web framework in Python. It utilizes a pre-trained Random Forest Regression model to estimate the selling price of a used car. Here's how the different components work together:

app.py: This is the main script that contains the Flask application and handles the routing and prediction logic. It defines two routes: the home route ("/") and the predict route ("/predict").
index.html: This HTML template file is rendered when the user accesses the home route. It displays a form where the user can enter the car details.
random_forest_regression_model.pkl: This is a pickled version of the trained Random Forest Regression model. It is loaded by the Flask application to make predictions.
StandardScaler: This class from scikit-learn is used to perform feature scaling on the input data.
The application accepts input for the following features:

Year: The year of the car. /n
Present_Price: The current market price of the car.
Kms_Driven: The total kilometers driven by the car.
Owner: The number of previous owners of the car.
Fuel_Type: The type of fuel used by the car (Petrol, Diesel, or CNG).
Seller_Type: The type of seller (Individual or Dealer).
Transmission: The type of transmission (Manual or Automatic).
Once the user submits the form, the input is processed by the Flask application. The categorical features are encoded appropriately, and the numerical features are scaled using the StandardScaler object. The preprocessed input is then passed to the trained model, which generates a prediction for the selling price. The prediction is displayed on the webpage.

If the predicted price is negative, the application displays a message stating that the car cannot be sold.
