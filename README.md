# D_Portfolio
Documentation of some of the projects I've worked on

# Project 1: Predicting obesity using classifier models on lifestyle and eating habits (tested using R)
## Data preprocessing
*	A dataset that compiled a group of participants' particulars and lifestyle habits, consisting of both categorical and numerical variables, was used.
*	Missing data was imputed.
*	One-hot encoding was carried out to convert categorical to numerical variables.
*	Data was scaled after being converted.
*	A correlation matrix was plot to identify any variables that may not have had any correlation to weight classification (target variable).

## Model Implementation
*	2 classifier models were built and tested, k-nearest neighbor (KNN) and random forest (RF)
*	Various ratios were tested when splitting the data into training and test sets but settled on a 70% - 30% split.
*	The square root of the number of samples was selected as the k-value.
*	A short loop was also written to plot the accuracy of the model vs the k-value as a means of visualizing the performance of the model with different parameters
*	For the RF model, the same split ratio was used as it was found to be optimal.
*	The RF model was tuned, testing various tree number values and different number of variables at each split.
*	Once the optimum values were obtained, the 2 models were benchmarked against one another with the RF model outperforming the KNN model in the case of this study.
 
# Project 2: Forecasting economic growth using econometrics and deep learning (tested using R and Python)
## Data preprocessing

* A timeseries dataset consisting of various economic but purely numerical variables was used.
* Given the nature of the data, there were no missing data or outliers.
* Data obtained was not homogeneous in terms of data frequency (some daily, some monthly, some quarterly)
* Daily data were aggregated to monthly average values using Excel and quarterly data were converted using temporal disaggregation using R.
* A total of 21 years worth of data was used and split into 18 years for training and 3 years for testing.

## Model Implementation

* A vector autoregression (VAR) model was tested as the econometric method while a seq2seq LSTM Network was tested as the deep learning method. 
* The VAR model was developed and had its assumptions tested (stationarity, autocorrelation, and heteroskedasticity).
* Due to certain violations of the assumptions, variables that were found to be in violation had to be removed.
* The model was rerun and evaluated before forecasting the economic growth for the year 2021.

* The LSTM Network was developed and additional data preprocessing was carried out as necessitated by the model.
* Tuning of the model hyperparameters were done by testing various hidden and dense layers across various epoch values. 
* A form of validation for timeseries analysis known as walk-forward validation was implemented for the model.
* The model was evaluated using the same evaluation metrics as the VAR model and the economic growth values for the year 2021 were forecasted.
* The evaluation metrics and the forecasted values of each model were then compared to each other as well as the official economic growth values as published by the Department  of Statistics, Malaysia (DOSM).
