# Forecasting-M3-experiments

Created by Elias Mayer ~ 25.08.2022
as a course submission for a ‘Forecasting’ module.


Simple R experiments conducted for a course assignment in the topic of forecasting. Please see the pdf report for a detailed desciption. 


Data sources: 

R library: Mcomp – N1355

R library: Mcomp – 70 quarterly time series of the M3 competition with IDs in [701, 1400] considering end numbers of 2 (702, 712, …).

See: https://cran.r-project.org/web/packages/Mcomp/index.html 


Process and outcome:

In the first step, an explanatory data analysis was conducted on the data set: N1355.
From this analysis, matching models for forecasting were chosen through a variety of measurements, including AIC values, time-series cross validation and test forecasts. 

The arima forecast performed the best out of these three methods and was estimated as an: (0,11)(0,1,1)[4] model. The ets model was estimated as an MMA model. The non-linear regression was constructed with knots to better fit the data but lead to inaccurate results due to over-fitting. 
Through batch processes, automatic model fits to the time series N0702, N0712, N0722, … , N1392 with different model types was conducted. 
A batch process for different automated exponential smoothing models was conducted. Also, a batch process for different automated arima models and a batch process for the Multiple Aggregation Prediction Algorithm (MAPA). 
Afterwards, a dynamic approach, which uses cross validation of the different automated methods to choose the best fitting model type and conduct a forecast, was implemented. 

All Batch processes lead to acceptable results. The dynamic approach and the automated arima model performed the best in a comparison of their MAPE (Mean absolute percentage error) scores. 

In the last experiment, a hybrid (combined) forecast model on the basis of: arima, ets and naïve forecasting models, while also dynamically able to switch to MAPA for better results, was implemented and compared with the previous methodologies. This approach was not successful and underperformed the dynamic model. 
A mix of methods (hybrid, MAPA, dynamic) used in dependence of their sector performance was estimated to be most suitable for the time series. 


Relevant files:

Link to the pdf report: https://github.com/EliDerDeli/Forecasting-M3-experiments/blob/main/Forecast_report.pdf 

The code is split in markdown files, each of which is independentl usable. 



 
