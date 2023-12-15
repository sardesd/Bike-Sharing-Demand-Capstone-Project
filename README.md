# Bike-Sharing-Demand-Capstone-Project
Bike Sharing Demand Regression
Variables Description
Date: The specific day when the data was collected.
Rented Bike Count: The total number of bikes rented on a particular day.
Hour: The specific hour of the day when the data was recorded.
Temperature(°C): The outside temperature, measured in degrees Celsius.
Humidity(%): The amount of water vapor in the air, measured as a percentage.
Wind speed (m/s): The wind speed, measured in meters per second.
Visibility (10m): The visibility distance, measured in tens of meters.
Dew point temperature(°C): The temperature at which dew starts to form, measured in degrees Celsius.
Solar Radiation (MJ/m2): The amount of solar energy hitting a square meter of the ground.
Rainfall(mm): The amount of rain that fell on a particular day, measured in millimeters.
Snowfall (cm): The amount of snow that fell on a particular day, measured in centimeters.
Seasons: The season when the data was recorded (Spring, Summer, Autumn, or Winter).
Holiday: Whether or not the day was a holiday.
Functioning Day: Whether or not the day was a working day.
Data Preprocessing
Downcasting: A process where the data types of DataFrame columns are converted to more efficient types for optimizing memory usage.
Datetime operation: Used to engineer extra features.
Data Analysis
KDE plot: Used to look at target distribution.
Boxplots: Used to check for outliers.
Lineplots: Used for bivariate analysis to show the relationship between two different variables.
Model Building
For every single model, we:

Use the same preprocessed data.
Use some form of feature selection.
First fit the model normally, then with some hyperparameter tuning.
Use multiple metrics, but ultimately rely on R-square for interpretation.
Handle all of the data preprocessing in the machine learning pipeline itself using a ‘prep’ column transformer.
Conclusion
All three models - Polynomial Regression, XGBoost, and Random Forest - were able to predict the ‘Rented Bike Count’ with varying degrees of accuracy.

Polynomial Regression had a training R^2 of 0.79 and a test R^2 of 0.75.
XGBoost performed significantly better, with a perfect R^2 of 1.00 on the training data and 0.94 on the test data.
Random Forest also performed well, with an R^2 of 0.90 on the training data and an impressive 0.99 on the test data.
The Stacking model, which combined the Random Forest and XGBoost models, had performance metrics very similar to those of the XGBoost model.
