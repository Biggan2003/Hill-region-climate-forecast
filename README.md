# Hill Region Climate Change Forecast (1981-2060)

## Project Overview
This project analyzes 45 years of daily climate data (1981-2025) from a Hill Region and generates yearly forecasts up to 2060 using multiple time series models.

## Dataset Features
- YEAR: Calendar year (1981-2025)
- Day of the Year: Julian day (1-366)
- Relative Humidity: Daily average (%)
- Precipitation: Daily rainfall (mm/day)
- Tmax: Daily maximum temperature (°C)
- Tmin: Daily minimum temperature (°C)
- Trange: Daily temperature range (°C)

## Models Used

| Variable | Best Model | Test MAE |
|----------|------------|----------|
| Tmax | ARIMA(1,1,1) | 0.28°C |
| Tmin | Prophet | 0.22°C |
| Trange | Linear Regression | 0.32°C |
| Humidity | Prophet | 1.39% |
| Precipitation | ARIMA(1,1,1) | 1305 mm |

## Key Findings
- Tmax: Stable around 29.5°C throughout the forecast period
- Tmin: Gradual warming trend (+0.15°C per decade)
- Trange: Decreasing trend (nights warming faster than days)
- Humidity: Slow but steady increase
- Precipitation: High variability, forecast settles to historical mean (~4100 mm/year)

## Visualizations
The notebook includes comprehensive visualizations:
- Individual plots for each variable (1981-2060)
- Confidence intervals for forecasts
- Trend analysis with regression lines
- Combined overlay plots

## Forecast Results (2026-2060)

| Year | Tmax (°C) | Tmin (°C) | Trange (°C) | Humidity (%) | Precip (mm) |
|------|-----------|-----------|-------------|--------------|-------------|
| 2026 | 29.50 | 22.48 | 6.76 | 80.33 | 4128 |
| 2027 | 29.51 | 22.50 | 6.72 | 80.45 | 4100 |
| 2028 | 29.51 | 22.52 | 6.69 | 80.58 | 4112 |
| 2029 | 29.51 | 22.53 | 6.65 | 80.71 | 4107 |
| 2030 | 29.51 | 22.55 | 6.62 | 80.83 | 4108 |
| 2060 | 29.51 | 22.64 | 6.45 | 81.46 | 4108 |

## How to Use
1. Clone this repository
   git clone https://github.com/Biggan2003/Hill-region-climate-forecast.git
   cd Hill-region-climate-forecast

2. Install requirements
   pip install -r requirements.txt

3. Open the Jupyter notebook
   jupyter notebook predicting-climate-change-in-hill-region.ipynb

## Requirements
numpy
pandas
matplotlib
seaborn
scikit-learn
statsmodels
prophet

## License
MIT License - Free to use for research and commercial purposes

## Links
- Kaggle Notebook: https://www.kaggle.com/code/gmbiggan/predicting-climate-change-in-hill-region
- Kaggle Dataset: https://www.kaggle.com/datasets/gmbiggan/historic-climate-data-hill-regian

## Author
G. M. Biggan
- GitHub: @Biggan2003
- Kaggle: https://www.kaggle.com/gmbiggan
