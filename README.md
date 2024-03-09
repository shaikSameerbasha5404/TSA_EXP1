# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
### Developed by:Shaik Sameer Basha
### Reference Number:212222240093
## POPULATION:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2015"].mean()
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()
```
## MARKET PRICE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
## TEMPERATURE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```








# OUTPUT:
## Population

![1 1](https://github.com/shaikSameerbasha5404/TSA_EXP1/assets/118707756/ddd0dc8d-4458-4741-803a-ab5f3bca3830)

## Stock price
![1 2](https://github.com/shaikSameerbasha5404/TSA_EXP1/assets/118707756/0f95a6d1-8f57-449f-85c5-72c1237a2130)

![1 3](https://github.com/shaikSameerbasha5404/TSA_EXP1/assets/118707756/a728d5a4-8b44-451b-8c47-898a4b0d9567)

## Temperature

![1 4](https://github.com/shaikSameerbasha5404/TSA_EXP1/assets/118707756/1b6e7775-844b-41e8-8842-96f73dfe3803)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
