# Forecasting California Unemployment
This project uses time series analysis to model and forecast unemployment counts in California using data from the Bureau of Labor Statistics. Using ARIMA modeling techniques in R, the goal was to identify the best-fitting model and evaluate its forecasting accuracy on real-world post-training data.

## Summary
- Data Source: [Kaggle - Unemployment in America, per US state](https://www.kaggle.com/datasets/justin2028/unemployment-in-america-per-us-state)
- Time Range: January 2010 – December 2018 (training), with 2019 used for testing
- Transformations: Square root transformation selected via Box-Cox analysis
- Model Selection: Evaluated ARIMA(2,1,0), ARIMA(4,1,0), ARIMA(2,2,0), ARIMA(4,2,0) using AICc and residual diagnostics
- Best Model: ARIMA(4,2,0), which passed all statistical diagnostic tests and produced accurate forecasts

## Tools & Packages
- R & RMarkdown
- `forecast`
- `dplyr`
- `lubridate`
- `MASS`
- `MuMIn`

## Project Structure
- `unemployment_forecasting.Rmd`: Main RMarkdown file with full time series analysis and forecasting
- `unemployment.csv`: Raw dataset (California subset)
- `unemployment_ts_report.pdf`: Written summary report with findings and conclusions
- `plot.roots.R`: Helper function for AR root plotting
- `README.md`: Project overview

## Forecasting Results
The ARIMA(4,2,0) model accurately forecasted 12 months of unemployment data post-2018, with predictions falling within the confidence intervals.

## How to Run
To reproduce this project:
1. Clone this repository or download the ZIP
2. Open `unemployment_forecasting.Rmd` in RStudio
3. Make sure `unemployment.csv` and `plot.roots.R` are in the same folder
4. Knit the RMarkdown file to generate outputs and forecasts

## View Project Deliverables
- [Full analysis report (HTML)](https://sath-parimi.github.io/ca-unemployment-forecasting/unemployment_forecasting.html): Knitted RMarkdown showing all code, plots, and diagnostics
- [Written summary report (PDF)](unemployment_ts_report.pdf): A formal write-up of the approach, findings, and conclusions

## Author
**Sathvika Parimi**  
B.S. Financial Mathematics and Statistics, UC Santa Barbara
