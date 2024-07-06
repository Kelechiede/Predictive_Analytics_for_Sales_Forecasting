## Insights and Conclusions from Sales Forecasting

### Overview of the Sales Data
The dataset comprises retail sales data from January 1992 to March 2023, containing 375 data points. Below are the summary statistics of the sales data:

- **Count:** 375
- **Mean:** 458,859.81
- **Standard Deviation:** 69,599.89
- **Minimum:** 318,525.69
- **25th Percentile:** 421,259.80
- **Median (50th Percentile):** 460,236.66
- **75th Percentile:** 500,209.47
- **Maximum:** 626,994.92

### ARIMA Model Findings
The ARIMA model was fitted to the training set (80% of the data) and used to forecast the test set (remaining 20%). Key findings include:

- **ARIMA Forecast Values:**
2017-01-01: 513,152.88
2017-02-01: 513,115.26
2017-03-01: 513,151.31
2017-04-01: 513,211.70
2017-05-01: 513,235.42
...
2022-11-01: 513,236.81
2022-12-01: 513,236.81
2023-01-01: 513,236.81
2023-02-01: 513,236.81
2023-03-01: 513,236.81
- **ARIMA Model RMSE:** 60,011.22

The ARIMA model shows consistent forecast values around the same range, indicating it captures the general trend but lacks in capturing variability in the data.

### LSTM Model Findings
An LSTM model was also trained and used for forecasting. The training process involved 100 epochs to minimize the loss function. Key findings include:

- **LSTM Forecast Values:**
2017-01-01: 512,333.44
2017-02-01: 519,283.69
2017-03-01: 521,129.84
2017-04-01: 520,077.94
2017-05-01: 519,438.22
...
2022-11-01: 607,445.31
2022-12-01: 610,052.56
2023-01-01: 600,964.63
2023-02-01: 596,131.94
2023-03-01: 606,573.38
- **LSTM Model RMSE:** 20,171.51

The LSTM model captures more variability in the sales data and shows closer forecast values to the actual sales data compared to the ARIMA model.

### Comparison of ARIMA and LSTM Models
The comparison of the ARIMA and LSTM forecasts against the actual sales data is summarized below:

| Date       | Actual Sales | ARIMA Forecast | LSTM Forecast |
|------------|---------------|----------------|---------------|
| 2017-01-01 | 515,053.79    | 513,152.88     | 512,333.44    |
| 2017-02-01 | 513,991.12    | 513,115.26     | 519,283.69    |
| 2017-03-01 | 513,345.35    | 513,151.31     | 521,129.84    |
| 2017-04-01 | 514,819.86    | 513,211.70     | 520,077.94    |
| 2017-05-01 | 512,201.83    | 513,235.42     | 519,438.22    |
| ...        | ...           | ...            | ...           |
| 2022-11-01 | 599,465.86    | 513,236.81     | 607,445.31    |
| 2022-12-01 | 594,087.03    | 513,236.81     | 610,052.56    |
| 2023-01-01 | 605,764.05    | 513,236.81     | 600,964.63    |
| 2023-02-01 | 600,477.34    | 513,236.81     | 596,131.94    |
| 2023-03-01 | 595,414.00    | 513,236.81     | 606,573.38    |

### Detailed Forecasts

#### ARIMA Model Forecast Details
The ARIMA model forecast details for the test period are shown below:

| Date       | Actual Sales | ARIMA Forecast |
|------------|---------------|----------------|
| 2017-01-01 | 515,053.79    | 513,152.88     |
| 2017-02-01 | 513,991.12    | 513,115.26     |
| 2017-03-01 | 513,345.35    | 513,151.31     |
| 2017-04-01 | 514,819.86    | 513,211.70     |
| 2017-05-01 | 512,201.83    | 513,235.42     |
| ...        | ...           | ...            |
| 2022-11-01 | 599,465.86    | 513,236.81     |
| 2022-12-01 | 594,087.03    | 513,236.81     |
| 2023-01-01 | 605,764.05    | 513,236.81     |
| 2023-02-01 | 600,477.34    | 513,236.81     |
| 2023-03-01 | 595,414.00    | 513,236.81     |

#### LSTM Model Forecast Details
The LSTM model forecast details for the test period are shown below:

| Date       | Actual Sales | LSTM Forecast  |
|------------|---------------|----------------|
| 2017-01-01 | 515,053.79    | 512,333.44     |
| 2017-02-01 | 513,991.12    | 519,283.69     |
| 2017-03-01 | 513,345.35    | 521,129.84     |
| 2017-04-01 | 514,819.86    | 520,077.94     |
| 2017-05-01 | 512,201.83    | 519,438.22     |
| ...        | ...           | ...            |
| 2022-11-01 | 599,465.86    | 607,445.31     |
| 2022-12-01 | 594,087.03    | 610,052.56     |
| 2023-01-01 | 605,764.05    | 600,964.63     |
| 2023-02-01 | 600,477.34    | 596,131.94     |
| 2023-03-01 | 595,414.00    | 606,573.38     |

### Conclusions
1. **Performance Comparison:** The LSTM model outperforms the ARIMA model in terms of RMSE, with values of 20,171.51 for LSTM and 60,011.22 for ARIMA, indicating that LSTM provides more accurate forecasts.
2. **Forecast Details:** The LSTM model captures the variability and trends in the sales data better than the ARIMA model, which tends to produce more stable but less variable forecasts.
3. **Actionable Insights:** For practical forecasting and business planning, the LSTM model is preferable due to its superior performance in capturing the dynamics of sales data. This model should be utilized for future sales predictions to achieve better accuracy and reliability. lues:** recast Values:**

