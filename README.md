# Energy_consumption_prediction
Purpose: analysis of articles and search for the most optimal machine learning model for forecasting electricity consumption, which can improve already existing indicators.

In this work, a study of 15-minute and hourly data sets "Steel industry energy consumption" collected from the Korean steel factory DAEWOO was conducted. After the preliminary analysis, certain data cleaning and preparation of sets for splitting into train and test samples was performed. The analysis showed that all features in the datasets affect the prediction result. It was also found that the 15-minute set is completely converted into the hourly set, that is, the total value of the 4 entries of the 15-minute set was equal to 1 value of the hourly set. During the analysis, there were certain observations, such as the fact that there was significantly less electricity use on weekends.

First, a simple linear regression model was used to compare the results of the metrics with the articles, namely MAPE, MAE, RMSE. As a conclusion, the results were almost identical. The possibility of predicting hourly consumption using a 15-minute set was also tested. A 15-minute set was trained and predicted, after which the data was converted to hourly. The result showed that forecasts of hourly recruitment using such a technique became more accurate.

Next, the multilayer perceptron (MLP) and Cubist models were used. Hyperparameters were selected using cross-validation, and TimeSeriesSplit was also applied, which made it possible to preserve the chronological order in the data and perform training on the past and validate on the future. This was done because the goal was to predict exactly future energy use, and it could also improve the accuracy of the models.

After the selection of hyperparameters, training of models and prediction of test samples and determination of quality metrics were performed. By comparing the metrics with the articles, it was found that both proposed models improve the results and forecasting accuracy. The Cubist method proved to be the best.
