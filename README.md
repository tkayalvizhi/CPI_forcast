# CPI forcast
This project was done as part of the **Data Analysis: Statistical Modeling and Computation in Applications course** [MITx MicroMasters in Statistics and Data Science]( https://micromasters.mit.edu/ds/ )

The goal of this problem is to analyze the CPI and BER data for the last decade. The CPI (consumer price index, the price of a "market basket of consumer goods and services" - a proxy for inflation) is released monthly by the Bureau of Labor Statistics, and is given in [CPI.csv](https://github.com/tkayalvizhi/CPI_forcast/blob/f7273ba5c94cba0d636b8ff39280075b45bcc150/CPI.csv). The file [T10YIE.csv](https://github.com/tkayalvizhi/CPI_forcast/blob/f7273ba5c94cba0d636b8ff39280075b45bcc150/T10YIE.csv) lists (during most of the same time period) the break-even rate (BER) , or the difference in yield between a fixed rate and inflation adjusted 10 year treasury note. This difference can be interpreted as what the market views will be the inflation rate for the next 10 years, on average.

[CPI_forecast.ipynb](https://github.com/tkayalvizhi/CPI_forcast/blob/f7273ba5c94cba0d636b8ff39280075b45bcc150/CPI_forecast.ipynb) develops a SARIMAX model for the **1 month ahead forecasts**

## Steps involved
1. Plot the monthly CPI value as a time series and observe trends
2. Detrend CPI data
3. Fit an Autoregressive model (without external regressors) and determine the appropriate lag
4. Determine the parameters of the Autoregressive model
5. Compute Root Mean Squared Error
6. Convert CPI monthly values to montly inflation rates (MIR)
7. Repeat steps 1-5 for the monthly inflation rates (MIR)
8. Resample daily BER data to get monthly BER data
9. Compute cross correlation between CPI and BER
10. Develop an Autoregressive model with monthly BER as external regressor 
11. Compute Root Mean Squared Error
