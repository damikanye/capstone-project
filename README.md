## Examine the rate at which suicide is commited

Suicide rates are decreasing globally of those countries that show clear linear trends over time, 2/3 are decreasing on average, suicide rate increases with age. This remains true when controlling for continent in the Americas, Asia & Europe, but not for Africa & Oceania. 

There is a weak positive relationship between a countries GDP (per capita) and suicide rate the highest suicide rate ever recorded in a demographic (for 1 year) is 225 (per 100k population).
There is an overrepresentation of men in suicide deaths at every level of analysis (globally, at a continent and country level). Globally, the male rate is ~3.5x higher. Africa has very few countries providing suicide data.

* <b>Loading the Dataset</b>: The dataset used is a collection of Suicide datasets and can be found [here](https://www.kaggle.com/russellyates88/suicide-rates-overview-1985-to-2016) – download it. Once you have downloaded the dataset, open your jupyter notebook and let’s get to work. Our first step is to load in the data using pandas read_csv function.

```python
import pandas as pd
df = pd.read_csv('master.csv')
```
![Jupyter](images/Capture.PNG)

* <b>Cleaning the Dataset</b>: Observing the dataframe, we will notice how we have 2/3 of HDI missing. We will drop <b>"HDIForYear"</b> and <b>"CountryYear"</b> because they’re not useful for our visualization. 

```python
#Drop the columns not needed
df.drop(["HDI for year",'country-year'],inplace=True,axis=1)
```

##Data Visualization 
