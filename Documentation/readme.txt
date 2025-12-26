Aim: To forecast ground-level O3 and NO2 for 24-hour (i.e., 1-day) at hourly interval for Delhi
•	Data (July 2019 - June 2024: 5 years) at hourly interval are provided for 7 sites in CSV format along with headers. (First develop your model for any one site, and later try with other sites)
•	Input parameters: year, month, day, hour, O3_forecast, NO2_forecast, T_forecast, q_forecast, u_forecast, v_forecast, w_forecast, NO2_satellite, HCHO_satellite, ratio_satellite 
•	Parameters to be estimated: O3_target, NO2_target (These are true measured values in ugm-3)
•	Use “site_X_train_data.csv” (X is a site number) to train and test your model. You can divide this data into 75%-25% to develop your model. Data are shuffled for different days, but in order over 24 hours.
•	Use “site_X_unseen_input_data.csv” as input data for the final validation of the model. True value of O3_target, NO2_target corresponding to this input data will be provided during the hackathon. That will decide the accuracy of your model. 
•	Note: 
o	Parameters with “forecast” label are from the reanalysis model
o	Satellite observations (i.e., NO2_satellite, HCHO_satellite, ratio_satellite) are once in a day (not hourly interval). It is challenging to effectively utilise these data in your model. If you do not find solution how to utilise it, drop the ‘satellite’ data and go ahead with ‘forecast’ data.
o	If you want to estimate O3_target and NO2_target for a given day, the input parameters (forecast as well as satellite) of the same day should be used. Additionally, if you wish to use past data, past 7 days of “O3_target”, and “NO2_target” could be used. 
o	Matrices to evaluate your model: RMSE (Root mean square error, unit: ugm-3), R2, and RIA (Refined Index of Agreement)




