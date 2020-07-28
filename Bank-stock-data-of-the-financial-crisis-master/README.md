# Bank stockes data from the financial crisis
The project analyses the the prices of some bank stocks and and their progresses throughout the financial crisis (2007-08) all the way to early 2016. The dataset contains stock information for the following banks:
*  BAC: Bank of America
* C: CitiGroup
* GS: Goldman Sachs
* JPM: JPMorgan Chase
* MS: Morgan Stanley
* WF: Wells Fargo

## Code
The code for the exploratory data analysis can be found [here](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/Bank-stock-data-of-the-financial-crisis-master/04-Finance_project%20_code.ipynb)

# Project Report
## Explore the data
### The max Close price for each bank's stock throughout the time period
```python
df.xs(key='Close',axis=1,level='Stock Info').max()
```
### The return values are  now created and stored in dataframe called returns usning pandas pct_change() method on the Close column.
```python
returns = pd.DataFrame()
for tick in tickers:
    returns[tick+' Return'] = df[tick]['Close'].pct_change()
returns.head()
```
### Inspect the date of the largest drop and biggest gain of the bank stockes
```python
returns.idxmin()
```
```python
returns.idxmax()
```
### The riskiest stock (corresponding to the highest std) for the year 2015 can be found using standard deviation method .std()
```python
returns.ix['2015-01-01':'2015-12-31'].std()
```

## Data Visualization
### A line plot showing Close price for each bank for the entire index of time
![Image description](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/Bank-stock-data-of-the-financial-crisis-master/Plots/Close_price.png)

### Moving Averages
Analyse the moving averages for these stocks in the period 2007-2009 BAC. 
![Image description](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/Bank-stock-data-of-the-financial-crisis-master/Plots/moving_average_BAC.png)

### Clustermap to cluster the correlations between the bank stockes
![Image description](https://github.com/lamdoanduc/Exploratory-data-analysis-projects/blob/master/Bank-stock-data-of-the-financial-crisis-master/Plots/clustermap.png)

# Important notes
* The method DataFrame.xs is very useful to take a key argument to select data at a particular level of a MultiIndex.
* Using Dataframe.rolling() to provide rolling window to calculate the averages.
