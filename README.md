# Microbusiness-Density-Forecasting-Project
Prediction of Micro-business concentration in a geographic area. 

This project is focused on predicting microbusiness density data for 3135 US counties using a simple GRU (Gated Recurrent Unit) model. The data used in the project spans from August 1, 2019, to December 31, 2022, totaling 41 months of data for each county. The goal of the project is to forecast the next five months of microbusiness density data for each county using the trained GRU model.

Here is a description of this project:-

Data Collection: Historical microbusiness density data for the 3135 US counties was collected from August 1, 2019, to December 31, 2022. This data is used to train and validate the GRU model.

GRU Model: The project uses a simple GRU model for time series forecasting. GRU is a type of recurrent neural network (RNN) that is capable of handling sequential data and capturing temporal dependencies. The architecture of the GRU model might include one or more GRU layers followed by dense layers for prediction.

Training and Validation: The 41 months of historical data for each county are split into multiple time windows for training and validation. The model is trained using 35 months of data over 18 historical time windows. The goal is to find the best set of hyperparameters and weights for the GRU model.

Validation Metric: The Simple Mean Absolute Percentage Error (SMAPE) score is used to evaluate the performance of the model during the validation phase. The SMAPE score measures the accuracy of the model's predictions relative to the actual values and provides a percentage indicating the average percentage error.

Model Tuning: The GRU model is tuned to maximize the local Cross-Validation (CV). Cross-validation is a technique used to assess how well a model generalizes to new data. Tuning the model to maximize local CV means selecting hyperparameters and model settings that result in the best performance across different cross-validation folds.

Forecasting: After training and validating the GRU model, it is used to forecast the next five months of microbusiness density data for each county. To make these forecasts, the model uses data from the last twelve months, leveraging the temporal patterns and dependencies it learned during the training phase.


Motivations for this project:
1) These forecasts can be valuable for various purposes, such as economic planning, resource allocation, and decision-making in the context of microbusinesses across different regions in the United States.
2) Risk Assessment: Financial institutions and investors can use the predicted microbusiness density data to assess risk when considering providing loans or funding to businesses in specific regions.
3) Real Estate and Commercial Development: The predictions can influence commercial real estate development decisions.
4) Benchmarking Performance: Comparing actual microbusiness density against the predicted values can help gauge the effectiveness of local economic development initiatives and policies.


Datasets used:
1) /kaggle/input/godaddy-microbusiness-density-forecasting
2) /kaggle/input/census-data-for-godaddy
3) /kaggle/input/godaddy-gru-98
