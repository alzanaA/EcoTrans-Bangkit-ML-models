# Install

This project requires Python and the following Python libraries installed:

- NumPy
- Pandas
- Matplotlib
- Tensorflow 


# Dataset

Datasets that are used to make the model are obtained from the first party so that the validity of the data can be maintained. Here is a link for each dataset:

1. [AQI Dataset](https://archive.ics.uci.edu/ml/datasets/Beijing+Multi-Site+Air-Quality+Data)

2. [Temperature Dataset](https://www.meteoblue.com/en/weather/archive/era5/jakarta_indonesia_1642911?daterange=2019-01-01%20-%202019-12-31&min=2019-01-01&max=2019-12-31&params%5B%5D=&params%5B%5D=temp2m&params%5B%5D=&params%5B%5D=precip&params%5B%5D=relhum2m&params%5B%5D=&params%5B%5D=wind%2Bdir10m&params%5B%5D=&params%5B%5D=totalClouds&params%5B%5D=&params%5B%5D=swrad&params%5B%5D=uvrad&params%5B%5D=&params%5B%5D=&params%5B%5D=&utc_offset=7&timeResolution=hourly&temperatureunit=CELSIUS&velocityunit=METER_PER_SECOND&energyunit=watts&lengthunit=metric&degree_day_type=10%3B30&gddBase=10&gddLimit=30)

3. [UV Index Dataset](https://docs.ambeedata.com/#weather-history-geospatial)

# Code

![image](https://user-images.githubusercontent.com/68011329/173268847-331eac8e-455c-48a4-8374-dcecd310aaa0.png)

Our models are using stacked LSTM and 2 hidden layers so that our models can add a level of abstraction in order to represent the problem at different time scales.


# Result

## 1. Temperature

![image](https://user-images.githubusercontent.com/68011329/173269357-7d67d5d3-9b6d-41f0-b5f4-a9ba70d62e78.png)

Above is the result of temperature. The orange line represent the forecasted value and the blue lines represent the actual value. The MAE of this model is 0.6392796 from the data range 0-40.

## 2. UV Index

![image](https://user-images.githubusercontent.com/68011329/173269569-804b493c-13b8-4328-92bd-a04616f20779.png)

Above is the result of uv Index.The orange line represent the forecasted value and the blue lines represent the actual value. The MAE of this model is 0.4844505 from data range 1-10.

## 3. AQI 

![image](https://user-images.githubusercontent.com/68011329/173269720-e623d3d1-6339-46f0-83cc-877763141a4c.png)

Above is the result of AQI (PM2.5).  The orange line represent the forecasted value and the blue lines represent the actual value. The MAE of this model is 2.470957 from data range 0-240.

# Run

Below is the sample image that show how to get the next _n_ hours that can be used for AQI (PM2.5), Temperature, UV Index.

![image](https://user-images.githubusercontent.com/68011329/173270247-6082cb25-839f-4d7a-8284-94231ead1cc5.png)
