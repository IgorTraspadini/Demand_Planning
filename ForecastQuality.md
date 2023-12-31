## Why some forecasts are better than others
The error in a forecast, or the residual, is the actual value that occurs minus the forecast.
Forecasts one and two are more accurate than forecasts three and four. That's because we're off by two units in forecasts one and two. 
Forecasts three and four, we see we're always off by five units so you might think these forecasts are sort of identical in quality, but that's not the case. We see with forecast three, sometimes we're too high, and sometimes we're too low. 
In forecast four, we see the error is always negative. It means the actual is less than the forecast, exhibits a 'bias'. We're systematically biased in the sense that our errors are negative, which means that our forecasts were too high. 

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/eef051ba-0305-438a-9988-57a8f302751c" width=50%>

### Mean Absolute Deviation (MAD)
If you get average of the erro (sales - forecast) the positive errors and the negative errors always cancel out if you don't take absolute values, and that's why we had to take absolute values, because otherwise every set of forecasts would look like it was equally good, because the average error was zero. If all your errors are zero, you're MAD will be zero, and that's your benchmark.

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/91c79b69-94c2-490f-8d7b-87bbbac13ca8" width=50%>

### Mean Absolute Percentage Error (MAPE)
Percentage error is the actual value of the series minus the forecasted value, divided by the actual value, and then the MAPE is the average of the absolute percentage errors. 
Now the question is, which of these series are doing a better job of forecasting? The forecast from series one or the forecast from series two in terms of accuracy. 
Well this is trickier than you might think. So let's look at the forecast MAD for each series. The MEAN absolute deviation for series one is three units. We're off by an average of three units. The MEAN absolute deviation for the forecast for series two is ten. So we're off by an average of ten units. So based on MAD, it looks like series two had worse forecast. Or series one had better forecast. But that's probably not really the way things are. Let's look at the percentage error, which is what most people in the business world use to measure their forecasts. So if you look at series one, we're off around ten percent per month. If you look at series two we're off about three percent per month. So we're much better off from percentage error standpoint in forecasting series two. Because you have to look at the size of your error, relative to what your forecasting. And you can see from series two we're up by only three percent, which is much better than ten percent. Even though the absolute average error is higher, the percentage error is lower.

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/88cf2297-0dad-4ba5-8ead-ebaad416e60e" width=50%>

### Sum of Squared Errors (SSE)
The definition is very simple, you simply compute the error for each observation which is actual minus predicted or forecasted, and then you square those errors and add them up. The purpose of squaring the errors is basically negative errors count the same as positive errors and don't cancel out. 
For all three of these measures of forecast accuracy, the MAD, the MAPE, and the SSE, lower is better, higher is worse.

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/a902aacd-1bb3-424d-bb84-488fc7ba271a" width=50%>

### Forecast Bias
When you think of the word bais, you probably think of the word prejudice. But essentially, bias in the forecasting world means your forecasts are either systematically too high, or systematically too low. So how do we determine if forecasts are biased? Bais is, are you sort of off too far in one direction or the other? Basically you compute, for every observation, the actual value divided by the forecast minus one. And if you average those numbers and they're close to zero, that would mean that your forecasts are not biased upward or downward. 
In forecast two they're all negative. What does that mean? The actual sales was less than the forecast in every case. Some of the time, actual sales should be higher than the forecast, and some of the time actual sales should be lower than a forecast. You can see we have more serious bias in forecast two than we have in forecast one.

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/94898153-55f0-4965-a1fd-aeaa9ade55d9" width=50%>

### Determining significance
The question naturally presents itself: which, if any, of these biases are statistically, significantly different from zero? The way statisticians answer this question is they compute a 95 percent confidence interval for the quantity of interest, in this case bias.
If zero is in the 95 percent confidence interval, the bias is not significant. If zero is not in the 95 percent confidence interval the bias is significant.

Now we can use these formulas to compute the 95 percent confidence interval for the bias for each of our two forecasts. 
So this means we're 95 percent sure the mean bias for forecast one is between -15 and 37 percent. That includes zero, so the bias is not significant. In other words, we really can't conclude that this bias indicates something that's statistically significantly different from a zero bias. 

We're 95 percent sure that for forecast two the mean bias is between -14 and -29 percent. That doesn't include zero, so that bias is significant. In other words, there is a significant bias in the forecast made for series two. 
What should the business person do in this situation? Try and understand why the bias exists. In other words, why are the actuals significantly higher than our forecasts? Because acting on bias forecast is going to cause the company lots of problems. It might cause a company to make too much of a product and result in excess inventory.

<img src="https://github.com/IgorTraspadini/Demand_Planning/assets/126266157/d4eeb24c-bf4d-4323-af7c-b4423fb639ef" width=100%>
