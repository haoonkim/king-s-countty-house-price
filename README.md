King County Housing Price Prediction
This project builds a regression model using TensorFlow and Keras to predict housing prices in King County, Washington, based on features such as square footage, number of bedrooms/bathrooms, year built, and more.

Dataset
File: kc_house_data.csv

Rows: 21,597

Columns: 21

Target Variable: price

Exploratory Data Analysis (EDA)
Performed using pandas, matplotlib, and seaborn:

Visualized price distribution and bedroom counts

Checked for missing values (none found)

Found top correlations with price:

sqft_living: 0.70

grade: 0.67

sqft_above, sqft_living15, bathrooms

Data Cleaning and Feature Engineering
Dropped non-informative columns: id, zipcode, date

Converted date to datetime format and extracted year, month

Applied MinMaxScaler to normalize numerical values

Model Architecture
Framework: TensorFlow/Keras

Type: Fully connected neural network

Hidden Layers: 4 layers with ReLU activation

Output Layer: 1 neuron with ReLU activation (for regression)

Optimizer: Adam

Loss Function: Mean Squared Error (MSE)

Epochs: 400

Batch Size: 128

Model Performance
Root Mean Squared Error (RMSE): ~163,452

Mean Absolute Error (MAE): ~101,088

Explained Variance Score: ~0.799

Training Visualization
Training and validation loss over epochs was plotted to confirm convergence and generalization.

Example Prediction
First house in dataset

Actual Price: $221,900

Predicted Price: $289,450

Libraries Used
pandas

numpy

matplotlib

seaborn

scikit-learn

tensorflow

Conclusion
The model is capable of predicting housing prices in King County with reasonable accuracy. Potential improvements include:

Hyperparameter tuning

Categorical feature encoding

Using alternative models like XGBoost or Random Forest

