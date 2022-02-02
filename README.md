# SBD_TimeSeries

Final Assignment
20220201

The individual assignment of the course Social Behaviour Dynamics is based on time series analysis, for which you need to have a time series dataset. Time series data consist of a large number (say more than 50) repeated measures of the same case. To give some examples:
-	Daily measurements of well-being and physical activity of a particular individual
-	Momentary conflict behaviors in a dyad (e.g., mother and child, or spouses)
-	Weekly sales of a company
-	Unemployment rates per month of a country


For the individual assignment, your data need to meet the following requirements:
-	You should have a continuous outcome variable (i.e., the variable you will try to predict and that you try to explain); it is ideal if this variable shows fluctuation up and down around a stable mean, or around some trend (e.g., a linear trend or a sinewave); it should not be entirely smooth. It is wise to find/collect more than one possible outcome variable to have a backup in case it doesn’t work out with your first choice.

-	You need at least three other variables that can be used as predictors, and that you can consider also as possible causes of the outcome variable; predictors and possible causes can be categorical (e.g., binary), but make sure that you also have continuous variables here.

-	You need at least 50 time points, but preferably more (say at least 100).

-	Keep in mind that you want to have variables that vary over time. For example, if you measure a variable like “headache severity”, it may be that this variable 99% of the time is equal to zero; this implies there is not a lot of variability in this variable.

## Dataset
The outcome variable is the total power load of electricity (unit: MW) per day in Taiwan. The data is daily measured and already aggregate the all records of power systems from different regions in Taiwan from 2017-01-01 to 2021-05-22, with 1603 observations. The data is provides by Taipower, the state-owned company which provides electricity to support the whole national energy demand, including both the public's quality of life and the economic development. 

The predictors: 

(1) `Temperature` (unit: Celsius degrees) -> When the temperature rise, especially over 28 Celsius degrees, people tend to turn on the air conditioners. The power usages of air conditioners could contribute significant increase of power load that highly relevant to the outcomes.

(2) `PrecpHour` (unit: hour) -> The precipitation hour gives insights into the humidity, sunshine time and weather conditions of that day. The precipitation could influence the apparent temperature of body feeling and human activities that cause different purposes of power usage. for example, in raining day people tend to stay at home that increase the power consuming from lights and home electronics.

(3) `Holiday_Type`-> The holiday includes weekday(0) from Monday to Friday; holiday(1) is Saturday and Sunday; national holiday(2) is the non-working day declared by Taiwan government. Because the majority of power consuming are from business-purpose activities and industries sectors, working hours cause notable electricity consuming compared to holidays. The holiday type is processed by the python code as the jupyter notebook.

Data from kaggle:
https://www.kaggle.com/patrick0302/taipower-eda/data
