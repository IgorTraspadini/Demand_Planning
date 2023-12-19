# Demand_Planning
How to create and evaluate forecasts?

We'll start by exploring the nature of time series data with scatter plots and moving average plots. Then we'll examine data bias and accuracy using methods including mean apps through deviation and sum of squared errors. Next we'll try out trend lines for forecasting. Then we'll model exponential growth, and compute CAGRs or compound annual growth rates. And finally, let's understand seasonality of data and how to forecast with multiple regression.

## What is time-series data?
Time-series data is a type of data that is collected or recorded over time at regular intervals. In time-series data, each data point is associated with a specific timestamp, allowing for the analysis of changes and trends over a continuous time period. This form of data is prevalent in various fields, including finance, economics, signal processing, weather forecasting, and many other domains where monitoring and analysis of changes over time are essential.

Some examples of time series are shown in bellow:
<table>
<tr>
  <td><img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/572d8f8e-837e-408e-a237-28c0f09a4340" width=100%></td>
  <td><img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/d5a53004-c461-4d12-b8fd-40933a574841" width=100%></td>
</tr>
<tr>
  <td><img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/0d7267bf-b464-4789-ad49-feebb6c821b4" width=100%></td>
  <td><img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/9b74b5fa-2e88-4ddd-b160-8e5e9e1a552b" width=100%></td>
</tr>
</table>

### Understanding level in a time series
The level of a time series describes the average value of the series.

- "Graph 1" you don't really see a change in level, there appears to be a steady level.
- "Graph 2" you can see the level of revenues increasing, which is plotted on the Y axis versus time is certainly not a steady level.
- "Graph 3" you can see the level decreasing.

![Level](https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/b7d9def9-c854-461a-ab8c-38cbdefe64fc)

### Understanding trend in a time series
Trend is simply the change in level from on period to the next in a time series.

- "Graph 1" there are no trend.
- "Graph 2" upward by 77% trend per year.
- "Graph 3" downward trend of 4% every 10 years.
- 
![Level](https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/b7d9def9-c854-461a-ab8c-38cbdefe64fc)

### Understanding seasonality in a time series
Basically by seasonality we mean a time series fluctuates consistently at regular intervals.

So if you look at this time series plot, you see a peak every fourth quarter. Every fourth quarter you see a peak. 

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/572d8f8e-837e-408e-a237-28c0f09a4340" width=50%>

### Understanding noise in a time series
Noise simply refers to random fluctuations in the time series about its typical pattern, but sometimes it's hard to identify the typical pattern.

- In "Graph 1" you can see there is fairly wide variation in the values about the dotted line. 
- In "Graph 2" in the early years, years one through eight, there is very little variation or noise about the pattern of the trendline, but you'll see in year 10 there is a lot of variation about the line. 

![Noise](https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/ef980ece-967e-487d-b9a7-4236ede84a54)

### Moving average
A moving average chart can help you better understand trend and level and smooth out what's going on with the time series, and also eliminate the influence of seasonal variation.
It eliminates seasonality because if you have a four-quarter moving average, you have one quarter from each quarter of the year and so none of the quarters of the year will have an undue influence on that chart.

Data:
- Quartely Data: create a four-quarter moving average chart, including the current quarter.
- Monthly Data: create a twelve-month moving average chart, including the current month.

![moving average](https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/451a795d-2f71-40bb-abff-ed5c5ffab209)

### Why some forecasts are better than others
The error in a forecast, or the residual, is the actual value that occurs minus the forecast.
Forecasts one and two are more accurate than forecasts three and four. That's because we're off by two units in forecasts one and two. 
Forecasts three and four, we see we're always off by five units so you might think these forecasts are sort of identical in quality, but that's not the case. We see with forecast three, sometimes we're too high, and sometimes we're too low. 
In forecast four, we see the error is always negative. It means the actual is less than the forecast, exhibits a 'bias'. We're systematically biased in the sense that our errors are negative, which means that our forecasts were too high. 

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/eef051ba-0305-438a-9988-57a8f302751c" width=50%>

### Mean Absolute Deviation (MAD)
If you get average of the erro (sales - forecast) the positive errors and the negative errors always cancel out if you don't take absolute values, and that's why we had to take absolute values, because otherwise every set of forecasts would look like it was equally good, because the average error was zero. If all your errors are zero, you're MAD will be zero, and that's your benchmark.

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/91c79b69-94c2-490f-8d7b-87bbbac13ca8" width=50%>

### Mean Absolute Percentage Error (MAPE)

