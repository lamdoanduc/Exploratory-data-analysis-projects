# 911-Calls
The project analyses calls to 911, i.e., what is the most reason of the calls, what high time people call 911, etc. The project also visualises the dataset using Seaborn and Bult-in Pandas tools. The dataset is from [Kaggle](https://www.kaggle.com/mchirico/montcoalert). 


## Code
The code for exploratory data data analysis can be found [here](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/911-Calls-master/911_calls_code.ipynb)

# Project report

The data contains the following fields:

* lat : String variable, Latitude
* lng: String variable, Longitude
* desc: String variable, Description of the Emergency Call
* zip: String variable, Zipcode
* title: String variable, Title
* timeStamp: String variable, YYYY-MM-DD HH:MM:SS
* twp: String variable, Township
* addr: String variable, Address
* e: String variable, Dummy variable (always 1)

## The reasons for the calls

![Image description](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/911-Calls-master/Plots/fig_countplot_reason_1.png)

## Charts showing number of calls by Month, Day of Week highlighted by Reason column

![Image description](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/911-Calls-master/Plots/calls_by_time.png)

## Linear Fit showing number of calls by month: groupby data by Month, then using count() funtion

![Image description](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/911-Calls-master/Plots/Number_of_calls_by_Month.png)

## Number of calls by days for the entire period

![Image description](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/911-Calls-master/Plots/Number_of_calls_by_time.png)

## The cluster shows high time of 911 calls

![Image description](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/911-Calls-master/Plots/heatmap.png)


