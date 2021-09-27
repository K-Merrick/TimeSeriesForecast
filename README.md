# TimeSeriesForecast
The purpose of this project was to build a machine learning model that forecasts taxi orders with an RMSE of no greater than 48. In carrying out this project, the following steps were taken:

    Resample the data into 1hr observations.
    Examine trends and seasonality of series.
    Check for stationarity with graphs and an Augmented Dickey-Fuller test.
    Check for autocorrelation.
    Perform differencing in order to obtain a stationary series.
    Train various Sklearn and gradient boosting regression models.
    Test the top 3 models and check them against a sanity check model.

Through training various models and optimizing hyperparameters using a validation dataset, we found that he CatBoost, LGBM, and Random Forest regressors provided the lowest RMSE score; that being said, each score using the validations dataset were far lower than the threshold of 48. In examining the performance of these models on the testing datasets, we found that both the CatBoost and Random Forest regressors provided scores below the threshold. Prior to concluding that we've built a model that can forecast taxi orders to a certain degree, we compared the RMSE scores of those models against a sanity check model, which simply used the immediately preceding value of an observation as the prediction. We found that our models' predictions were approximately 30% more accurate than the sanity model's. As such, we believe that our models do provide some functionality with regard to accurately forecasting taxi orders.
