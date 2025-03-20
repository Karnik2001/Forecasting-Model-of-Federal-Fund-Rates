# Forecasting Model of Federal Fund Rates

## Overview

This project applies a SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous factors) model to forecast the Federal Funds Rate (FFR) over the next 24 months.

## Importance of the Federal Funds Rate

The Federal Funds Rate (FFR) is a key economic indicator of U.S. monetary policy, influencing economic growth and unemployment rates. The Federal Reserve sets the FFR based on factors such as inflation and the equilibrium interest rate. Changes in the FFR affect borrowing costs for banks, influencing interest rates on loans, credit cards, and bank deposits.

A lower FFR makes it easier for banks to borrow funds and maintain the required 10% reserve ratio, facilitating increased lending to businesses and individuals. This, in turn, can stimulate economic growth by encouraging investment and spending. Conversely, raising the FFR helps control inflation by making borrowing more expensive, which can slow down economic activity.


## Diagnostic Tests

Ljung-Box Test (Q-Stat): 0.03 (p-value = 0.85) → No significant autocorrelation in residuals.

Jarque-Bera Test: 3,788,667.57 (p-value = 0.00) → Residuals are not normally distributed.

Skewness: -12.25 (indicating strong left-skewed distribution)

Kurtosis: 224.86 (indicating extreme peakedness in distribution)

Heteroskedasticity Test (H): 0.04 (p-value = 0.00) → Strong heteroskedasticity detected.

## Unit Root Test (ADF Test)

ADF Statistic: -0.126720

p-value: 0.946711

Critical Values:

1%: -3.434

5%: -2.863

10%: -2.568

Interpretation: The ADF test fails to reject the null hypothesis, indicating that the time series is non-stationary.

## Error Metrics

Mean Squared Error (MSE): 0.00358

Mean Absolute Error (MAE): 0.00504

## Key Observations from Forecast

The forecasted values remain flat, indicating no significant expected change in FFR.

The confidence interval widens over time, showing increasing uncertainty.

The lower bound of the confidence interval dips below zero, which may be unrealistic for FFR.

The high AR(1) coefficient (≈1) suggests possible non-stationarity, which could impact the model’s reliability.


## Citations
https://www.businessinsider.com/personal-finance/investing/what-is-the-federal-funds-rate
https://medium.com/swlh/forecasting-interest-rates-with-arma-649cbcd2d388
