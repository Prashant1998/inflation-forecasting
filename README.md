\# Inflation Forecasting using Macroeconomic Indicators



An applied time-series and machine learning project analyzing the limits of inflation forecasting using publicly available macroeconomic data.



\## Motivation



Inflation forecasting is central to economic policy and financial decision-making.

However, macroeconomic time series are noisy, small-sample, and subject to regime shifts.

This project evaluates whether machine learning meaningfully improves forecasts beyond classical baselines.



\## Data



Monthly U.S. macroeconomic data sourced from the Federal Reserve Economic Data (FRED):



\- Consumer Price Index (CPI)

\- Federal Funds Rate

\- Unemployment Rate

\- Industrial Production Index



Raw data is merged using inner joins to ensure temporal consistency and avoid implicit forward-filling.



\## Methodology



1\. Raw data ingestion and merging

2\. Exploratory data analysis

3\. Stationarity diagnostics and transformations

4\. Baseline forecasting models:

&nbsp;  - Naive (lag-1)

&nbsp;  - Rolling mean

&nbsp;  - ARIMA

5\. Machine learning models with lag features:

&nbsp;  - Linear Regression

&nbsp;  - Ridge Regression

6\. Time-aware train-test evaluation





\## Key Results



\- Persistence-based baselines provide a strong performance floor

\- ARIMA marginally improves accuracy but fails during regime shifts

\- Machine learning models add limited value beyond lag structure

\- Forecast errors increase sharply during macroeconomic stress periods



\## Example Forecast



See notebooks/05\_evaluation\_and\_insights.ipynb for forecast comparisons and error diagnostics.



\## Limitations



\- Monthly data limits sample size

\- Structural breaks violate stationarity assumptions

\- Real-time data release lags are not explicitly modeled



\## Future Work



\- Incorporating high-frequency and expectations data

\- Regime-switching or state-space models

\- Nowcasting using mixed-frequency inputs



\## Repository Structure



\- data/        Raw and processed datasets

\- notebooks/   Analysis and modeling notebooks

\- src/         Reusable utility code



