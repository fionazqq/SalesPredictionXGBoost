# SalesPredictionXGBoost
Rossman Store Scales Prediction Project - XGBoost
# Rossmann Store Sales Prediction

https://www.kaggle.com/competitions/rossmann-store-sales/overview

## Background

Rossmann, founded in 1972, is the largest grocery store in Germany with more than 3000 stores in 7 European countries. From time to time, the stores organize short-term promotions as well as continuous promotions to increase sales. In addition, store sales are influenced by many factors, including promotions, competition, school and national holidays, seasonality and cyclicality.

## Project Goal

After understanding the data we need to clarify the purpose of our project, in Rossmanns sales forecasting we need to use historical data, i.e. data in intrain.csv for supervised learning. The trained model is inferred (predicted) using the data in intrain.csv, and the predicted data is submitted to Kaggle as sample_submission.csv
The predicted data is submitted to Kaggle for scoring in the format of sample_submission.csv. This process can also be combined with the additional information in store.csv to enhance the ability of our model to obtain data.

## Data Overview

- train.csv - historical data including Sales
- test.csv - historical data excluding Sales
- sample_submission.csv - a sample submission file in the correct format
- store.csv - supplemental information about the stores


- Data fields: Most of the fields are self-explanatory. The following are descriptions for those that aren't.

**Data Features**

Id - an Id that represents a (Store, Date) duple within the test set

Store - a unique Id for each store

Sales - the turnover for any given day (this is what you are predicting)

Customers - the number of customers on a given day

Open - an indicator for whether the store was open: 0 = closed, 1 = open

StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note 
that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None

SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools

StoreType - differentiates between 4 different store models: a, b, c, d

Assortment - describes an assortment level: a = basic, b = extra, c = extended

CompetitionDistance - distance in meters to the nearest competitor store

CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened

Promo - indicates whether a store is running a promo on that day

Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store 
is participating

Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2

PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store
