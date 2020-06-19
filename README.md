### 1) EDA and Forecasting on weekly petrol and diesel data in the UK

Jupyternotebook links:
- <a href="https://nbviewer.jupyter.org/github/NyanoNyan/Portfolio/blob/59639bfcaf796363e91acf44e9b83818aa347953/1)%20EDA%20and%20Forecasting/Clean_EDA_weekly_road_fuel.ipynb">Exploratory Data Analysis (EDA) on weekly petrol and diesel data </a>

- <a href="https://nbviewer.jupyter.org/github/NyanoNyan/Portfolio/blob/8f090e46031668a77bcf0d93c0fad397fccafe0d/1)%20EDA%20and%20Forecasting/Clean_LSTM_Forecasting_weekly_road_fuel_without_trend.ipynb">LSTM forecasting **without Trend removal**</a>

- <a href="https://nbviewer.jupyter.org/github/NyanoNyan/Portfolio/blob/22201b5ecb361169cb0288bfdd76b4190e810b4e/1)%20EDA%20and%20Forecasting/Clean_LSTM_Forecasting_weekly_road_fuel.ipynb">LSTM forecasting **with Trend removal**</a>


<a href="https://gyazo.com/d2ff2a0d27b62e94887ea3a6a6dc7e22"><img src="https://i.gyazo.com/d2ff2a0d27b62e94887ea3a6a6dc7e22.gif" alt="Image from Gyazo" width="700"/></a>

Details about the data: 

- The data was for a weekly road fuel prices on the cost for the unleaded petrol (ULSP) and unleaded diesel (ULSD).

- Univariate forecasting method was used

- A 7 day windowed data size was chosen due to the data being weekly. Also, a weekly data would seem appropriate to choose to forecast future weeks. 

- A bidrectional LSTM was used form this model. L2 and dropout regularization were used to reduce overfitting.


### Forecasting without trend removal

- Training and testing loss
- Results on the training and validation are good as validation loss is lower compared to the training loss. This helps as the model will be able to predict future values better.

<img src="images/train and test loss.JPG" width="700">


- Results on training set shows that the predicted values are similar to the actual values.


<img src="images/training_data_results.JPG" width="700">


- Although, not perfect. The results from the predicted values from the test/validation data shows that it is able to predict similar trend compared to the actual test.

<img src="images/training_data_test_results.JPG" width="700">


- Predicting the future, 7 weeks into the future

<img src="images/future_predictions.JPG" width="700">
