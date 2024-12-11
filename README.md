# power-outages-data-analysis
This is from my DSC 80 final project that I work independently.

https://tachiu33333.github.io/power-outages-data-analysis/


Introduction:
Hello, welcome. On this site, you will find the data exploration of a dataset that was given to me through my DSC 80 class at UCSD. Below, you'll find that I am working with the power outage data with the data of state wide power outages taken place in United States from January 2000 to July 2016. I think when reading this dataset, the first question anyone has, including myself, is how this data can help understand how severe a disaster can be, and how it affects the general populace. This dataset is supported by columns such as cause categories and its detail, numbers of customers affected and the duration of the power outage loss.


I will create a model that tells the severity of a certain causes based on the number of people affected at certain places at certain times.
I think that companies not just want to predict causes but also know how much resources to allocate to those of certain causes. Knowing what type of accident happened and how bad it is can help scope how much might need to be recomopensated to reassist those affected.

When first given the excel file, there is 1540 rows and 57 columns. Without the rows that obstruct the actual dataframe, there is actually 1534 rows and 56 columns.

This dataset focuses on power outage failures documents across history.
Honestly, this can help us understand correlation with causes and how it affects outages. We can then at least have a prediction for how much resources we lost and how much effort we would have to strive for to make up for our losses.

Because of this I'll be using the following columns:


a.b.b.c.c.d.sd.a.f.sadf.as.df
    description of said columns.....

Data Cleaning:
The excel sheet actually had 1540 rows and 57 columns in total because it also included extra row of space, and extra columns for the title, and extra details to share. That means that i had to manually remove certain obvious columns such as the first 5 and the 7th column. The first 5 were all title and what the dataframe entails. The 7th column included smaller detail of each column. I also removed the variable column because it didn't mean anything at all.

From there, I also removed 'POSTAL.CODE' as it was exactly the same as US.State and I felt that state was easier to read. I removed OBS since the index already did its job for it. 'MONTH' and 'YEAR' were removed because start time and date as well as restoration time and data already answer that for me. Furthermore, each post is an event that happened. It would be weird if an outage applied on a saturday night and didn't go on to next morning.


Prediction Process step 5:
We are going to predict how many customers were affected if a disaster striked, based on the disaster itself.
There are ma



Goal:
determine where you live and where you are placed, cant the cause category between severe attack and intentional attack and system disruption and equipment failure can affect the number of customers affected.

MIssingness analysis:
based on the source, the dataset comes from the eia and doe data. Due to that, we can infer that the United State grabs their data from public and private sectors including surveys or private tours. We can then figure out that data that can only be accomplished by internals or external. means can only be avoided by nmar. The ones I feel strongly align with these reasons are...

Hypothesis:
There are more customers affected by outside reasons(severe attack/intentional attack) than internal reasons(system disruption/equipment failure)