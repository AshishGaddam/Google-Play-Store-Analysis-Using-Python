# Google-Play-Store-Analysis-Using-Python

## Objectives

Google Play Store team is about to lunch a new feature where in certain apps that are promising are boosted in visibility. The boost will manifest in multiple ways- higer priority inpromising are boosted in visibility. The boost will manifest in multiple ways – higher priority in recommendations sections (“Similar apps”, “You might also like”, “New and updated games”). These will also get a boost in visibility in search results. This feature will help bring more attention to newer apps that have potential. The task is to understand what makes an app perform well - size? price? category? multiple factors together? Analyze the data and present your insights in a format consumable by business – the final output of the analysis would be presented to business as insights with supporting data visualizations. 

## Task

1. Data clean up – Missing value treatment
a. Drop records where rating is missing since rating is our target/study variable
b. Check the null values for the Android Ver column.
i. Are all 3 records having the same problem?
ii. Drop the 3rd record i.e. record for “Life Made WIFI …”
iii. Replace remaining missing values with the mode
c. Current ver – replace with most common value
2. Data clean up – correcting the data types
a. Which all variables need to be brought to numeric types?
b. Price variable – remove $ sign and convert to float
c. Installs – remove ‘,’ and ‘+’ sign, convert to integer
d. Convert all other identified columns to numeric
3. Sanity checks – check for the following and handle accordingly
a. Avg. rating should be between 1 and 5, as only these values are allowed on the play
store.
i. Are there any such records? Drop if so.
b. Reviews should not be more than installs as only those who installed can review the
app.
i. Are there any such records? Drop if so.
4. Identify and handle outliers –
a. Price column
i. Make suitable plot to identify outliers in price
ii. Do you expect apps on the play store to cost $200? Check out these cases
iii. After dropping the useless records, make the suitable plot again to identify
outliers
iv. Limit data to records with price < $30
b. Reviews column
i. Make suitable plot
ii. Limit data to apps with < 1 Million reviews
c. Installs
i. What is the 95th percentile of the installs?
ii. Drop records having a value more than the 95th percentile
