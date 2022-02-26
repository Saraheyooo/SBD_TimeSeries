# SBD_TimeSeries

Final Assignment
20220201

The repository is using time series analysis within Social Behaviour Dynamics. Time series data consist of the amount of daily power load in Taiwan, which from Kaggle. We will look into the causal relationship using SARIMA model and Granger Causal analysis to forecast and discover the
inferences between the outcomes and predictors.


Data from kaggle:
https://www.kaggle.com/patrick0302/taipower-eda/data

## Dataset
The outcome variable is the total power load of electricity (unit: MW) per day in Taiwan. The data is daily measured and already aggregate the all records of power systems from different regions in Taiwan from 2017-01-01 to 2021-05-22, with 1603 observations. The data is provides by Taipower, the state-owned company which provides electricity to support the whole national energy demand, including both the public's quality of life and the economic development. 

The predictors: 

(1) `Temperature` (unit: Celsius degrees) -> When the temperature rise, especially over 28 Celsius degrees, people tend to turn on the air conditioners. The power usages of air conditioners could contribute significant increase of power load that highly relevant to the outcomes.

(2) `PrecpHour` (unit: hour) -> The precipitation hour gives insights into the humidity, sunshine time and weather conditions of that day. The precipitation could influence the apparent temperature of body feeling and human activities that cause different purposes of power usage. for example, in raining day people tend to stay at home that increase the power consuming from lights and home electronics.

(3) `Holiday_Type`-> The holiday includes weekday(0) from Monday to Friday; holiday(1) is Saturday and Sunday; national holiday(2) is the non-working day declared by Taiwan government. Because the majority of power consuming are from business-purpose activities and industries sectors, working hours cause notable electricity consuming compared to holidays. The holiday type is processed by the python code as the jupyter notebook.


