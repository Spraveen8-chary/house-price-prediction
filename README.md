# Home Price Prediction

This project is a Python-based web application that predicts the estimated price of a home in Bangalore, India, based on various input parameters such as the location, square footage (sqft), number of bedrooms (bhk), and number of bathrooms (bath). The prediction model used in this project is trained using machine learning techniques and is exposed through a Flask web server. Users can make HTTP requests to this server to obtain price predictions for different properties.

## Project Structure

The project consists of two main files:

- **util.py**: This module contains functions and data for loading the machine learning model and making price predictions. It includes the following key functions:
  - `get_estimated_price(location, sqft, bhk, bath)`: This function takes the property details as input and returns the estimated price of the property based on the trained machine learning model.
  - `load_saved_artifacts()`: This function loads the saved model and data columns from files and initializes global variables.

- **server.py**: This file sets up a Flask web server that exposes two API endpoints:
  - `/get_location_names` (GET request): This endpoint returns a list of available locations for which price predictions can be made.
  - `/predict_home_price` (POST request): This endpoint accepts property details as input in the request body and returns the estimated price as a response.

## Getting Started

Follow these steps to run the Home Price Prediction web application:

1. **Install Dependencies**: Make sure you have Python 3.x installed. Install the required Python packages listed in the `requirements.txt` file by running the following command:
   ```bash
   pip install -r requirements.txt
2. **Run the Server**: Execute the server.py script to start the Flask server:
   - The server will start and listen on a specified port (usually 5000) locally.

# API Usage
## 1. Get Available Locations
- To retrieve a list of available locations for which price predictions can be made, you can make a GET request to the following endpoint:

  ```bash
    GET http://localhost:5000/get_location_names

- This will return a JSON response containing a list of location names.

## 2. Predict Home Price
- To predict the estimated price of a home, you can make a POST request to the following endpoint:
  ```bash
    POST http://localhost:5000/predict_home_price

- You should include the following parameters in the request body:

- total_sqft: Total square footage of the property (float).
- location: The location of the property (string).
- bhk: The number of bedrooms (integer).
- bath: The number of bathrooms (integer).
- The server will respond with a JSON object containing the estimated price.

# Example Usage
You can use the provided Python script in util.py as an example of how to interact with the server. It demonstrates how to load the model, make predictions, and print the estimated prices for sample properties.

# Project Files
- util.py: Contains utility functions for data preprocessing and making predictions.
- server.py: Sets up the Flask server and defines API endpoints.
- artifacts: Directory containing saved model and data columns.
- requirements.txt: List of Python packages required for this project.

# Note
- The machine learning model used in this project is based on historical data and is trained to make estimations. Actual property prices may vary.
- The server allows cross-origin requests for easier integration with web applications. In production, it is recommended to restrict access based on your specific use case.

# Output 
![image](https://github.com/Spraveen8-chary/house-price-prediction/assets/108536707/446eaa55-f471-4cb8-8518-36702d0ed3bd)
