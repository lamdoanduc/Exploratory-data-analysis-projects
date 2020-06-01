# Polls of the 2012 election Data

The project analyzes a dataset of the the 2012 election from HuffPost Pollster to find the answer for the following questions: \
    1. Who was being polled and what was their party affiliation? \
    2. Did the poll results favor Romney or Obama? \
    3. How do undecided voters effect the poll? \
    4. Can we account for the undecided voters? \
    5. How did voter sentiment change over time? \
    6. Can we see an effect in the polls from the debates?
    
 # Report
 ## Request data from the web
 
 ```python
url='http://elections.huffingtonpost.com/pollster/2012-general-election-romney-vs-obama.csv'
source=requests.get(url).text

df_data=StringIO(source)
df = pd.read_csv(df_data)
df
```
## 1. Who was being polled and what was their party affiliation?

![Image description](https://github.com/lamdoanduc/Polls-of-the-2012-election/blob/master/plots/01_affiliation.png)

## 2. Did the poll results favor Romney or Obama? and 3. How do undecided voters effect the poll?

![Image description](https://github.com/lamdoanduc/Polls-of-the-2012-election/blob/master/plots/01_pool_results.png)

## 5. How did voter sentiment change over time?

![Image description](https://github.com/lamdoanduc/Polls-of-the-2012-election/blob/master/plots/01_sentiment_over_time.png)

## 6. Can we see an effect in the polls from the debates?

![Image description](https://github.com/lamdoanduc/Polls-of-the-2012-election/blob/master/plots/01_result_after_debates.png)


