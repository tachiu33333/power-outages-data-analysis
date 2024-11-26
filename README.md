# power-outages-data-analysis
This is from my DSC 80 final project that I work independently.

https://tachiu33333.github.io/power-outages-data-analysis/


Introduction:
There is 1540 rows and 57 columns.
Without the rows that obstruct the actual dataframe, there is actually 1534 rows and 56 columns.

This dataset focuses on power outage failures documents across history.

I think when reading this dataset, the first question anyone has, including myself, is how this data can help understand how severe a disaster can be, and how it affects the general populace. This data is supported by columns such as cause categories and its detail, # of customers affected and the duration of the power outage loss.

Honestly, this can help us understand correlation with causes and how it affects outages. We can then at least have a prediction for how much resources we lost and how much effort we would have to strive for to make up for our losses.

Data Cleaning:
The excel sheet actually had 1540 rows and 57 columns in total because it also included extra row of space, and extra columns for the title, and extra details to share. That means that i had to manually remove certain obvious columns such as the first 5 and the 7th column. The first 5 were all title and what the dataframe entails. The 7th column included smaller detail of each column. I also removed the variable column because it didn't mean anything at all.

From there, I also removed 'POSTAL.CODE' as it was exactly the same as US.State and I felt that state was easier to read. I removed OBS since the index already did its job for it. 'MONTH' and 'YEAR' were removed because start time and date as well as restoration time and data already answer that for me. Furthermore, each post is an event that happened. It would be weird if an outage applied on a saturday night and didn't go on to next morning.


Prediction Process step 5:
We are going to predict how many customers were affected if a disaster striked, based on the disaster itself.
There are ma