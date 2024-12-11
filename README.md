
https://tachiu33333.github.io/power-outages-data-analysis/

## **Introduction:** ##

Hello, welcome. On this site, you will find a data analysis on the U.S power outage from January 2000 to July 2016. You can find the dataset yourself at : https://engineering.purdue.edu/LASCI/research-data/outages. I'll be attempting to try my best to focus on a few questions throughout my analysis. The big overall theme is to understand the severity of these damages that the power outages bring. I hope that by the end of this, my model can help predict for companies in the strength of damages and how to reinforce for future damages to come.

Diving right in, when first given the excel file there is 1540 rows and 57 columns. Without the rows that obstruct the actual dataframe, there is actually 1534 rows and 56 columns. From there we cipher out data we do not need.

This dataset focuses on power outage failures documents across history.
Honestly, this can help us understand correlation with causes and how it affects outages. We can then at least have a prediction for how much resources we lost and how much effort we would have to strive for to make up for our losses.

Because of this I'll be using the following columns:

* 'YEAR', : Tells the year of the outage
* 'MONTH', : Tells the month of the outage
* 'U.S._STATE' : Tells the state of the outage
* 'NERC.REGION', : Tells the region/entity of United States that it is part of
* 'OUTAGE.START.DATE': tells the date of the outage
* 'OUTAGE.START.TIME': tells the time of the outage
* 'CLIMATE.REGION': Tells the region of United States
* 'CLIMATE.CATEGORY': Tells how warm the region was at the time of the outage
* 'CAUSE.CATEGORY', : Tells what type of damage was done (Severe Weather, Intentional Attack, System Disruption and Equipment Failure)
* 'CAUSE.CATEGORY.DETAIL': Specify into more about what cause the damage
* 'OUTAGE.DURATION', : Tells how long the outage took place
* 'DEMAND.LOSS.MW': tells how much energy was used in terms of mw during the outage
* 'CUSTOMERS.AFFECTED': tells how many customers complained during the outage
* 'RES.CUSTOMERS': Number of residential customers
* 'COM.CUSTOMERS': Number of commercial customers
* 'IND.CUSTOMERS': Number of industrial customers
* 'TOTAL.CUSTOMERS': Total number of customers at the time of the outage
* 'POPULATION': Complete population of the entire state
* 'POPPCT_URBAN': percentage of the state that lives in urban areas
* 'POPPCT_UC', : percentage of the state that lives in urban clusters
* 'POPDEN_URBAN': population density of the state that lives in urban areas
* 'POPDEN_UC',: population density of the state that lives in urban cluster
* 'POPDEN_RURAL': population density of the state that lives in rural areas


## Data Cleaning: ##
The excel sheet came with 1540 rows and 57 columns in total because it also included extra row of space, and extra columns for the title, and extra details to share. I started off by removing these extra spaces before moving on and removing several columns until I had the ones above. It's not like they will all make it to the final product, but they were all of use. Next I also filled in customers affected and outage duraiton to fill in the void. I also fixed a few columns like 'NERC.REGION' to make sure there wouldn't be any anomolies for later.


## Univariate Analysis: ##

<iframe
  src="Asset/frequency-cause.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>

This one is where I tried to figure out the number of each cause and get a feel for the data. I learn that the top 4 columns are there because the rest are ways to mitigate or fix problems after outages while the first three are actual problems.

## Bivariate Analysis: ##
<iframe
  src="Asset/customer_pop.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>

This graph was trying to see between population and Customers that were afffected by the storm. We would learn that population does not actually correlate with customers as I would've hope for, but the graph does look to have three hills signifying that the data might have had sweet points of customers affected and the right amount of people in a state.

## Interesting Aggregate: ##



## NMAR Corner: ##
The column 'DEMAND.LOSS.MW' was mentioned on the site that these data are either surveyed and straight froma a company who deals with these data. Because of that, we have to assume that those NaN values were a byproduct of those who didn't apply the information. However, as you'll see later, just like a lot of other column, it very much can be a MAR column because we can infer that the missing data might be able to be impute the missing information but for now, we have to accept the worst case scenario in where 'DEMAND.LOSS.MW' had data that wasn't shared.


## Missingness Depenedacy: ##



## Hypothesis Testing: ##

All this data about power outages are great for companies who are looking for better security against these unforseeen moements. Hence the idea is to then determine whether a company should invest in better security for themselves or against others and nature. The idea of this segment, is to understand the value of each CAUSE.CATEGORY and how mcuh value they actually have. Hence, outside issues are elements in CAUSE.CATEGORY that are 'severe weather' and 'intentional'. Inside issues are problem that include 'system operability disruption' and 'equipment failures'.


The following values below are stats after creating a permutation test 
* null: the difference between inside and outside issues are the same
* alternative hypotheses: the difference between inside and outsdie issues are significantly different.
* test statistic(difference in means): -19195.0049
* significance level: 0.05
* p-value: 0.3336

    # Conclusion: #
The p-value is much larger than the significance level, meaning we align with the null hypothesis than the alternative hypothesis in this case. Inside and outside issues have not as much difference between each other as I would've hope but this just means that moving forward, we can use CAUSE.CATEGORY without bias.


## Prediction Process: ##
We are going to predict how many customers were affected if a disaster striked, based on the disaster itself.

## Baseline Model: ##


## Final Model: ##




## Fairness Analysis: ##