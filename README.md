Table of Contents:

Index of Column Names and explanations

Business Concept and General Themes

Data cleaning, EDA methodology and Visualisations

Regression Models 

INDEX:

ID: A unique identifier for each house sale

Date: A value denoting the date of each sale

Price: The price for which each house was sold

Bedrooms: The number of bedrooms in a property

Bathrooms: The number of bathrooms in a property

Sqft_living: The square footage of the appartment's living space

Sqft_lot: The square footage of the lot the property is built on

Floors: The number of floors a property possesses

Waterfront: Denoting whether the property is on the waterfront or not

View: A scale from 0 - 4 denoting quality of view from the property

Condition: 1 (lowest) - 5 (highest) denoting structural/cosmetic state of the property

Sqft_above: The square footage of the house above ground level

Sqft_basement: The square footage of the basement below ground level

yr_built: The year the house was built

yr_renovated: The year the house was last renovated, if ever

zipcode: The zipcode in which the property is located

lat: The latitude co-ordinate of the house

long: The longitude co-ordinate of the house

sqft_living15: The square foot living space for the nearest 15 neighbours

sqft_lot15:  The square foot lot space for the nearest 15 neighbours

BUSINESS MODEL AND CONCEPT

The concept that we developed for the project was based on the old economics adage of 'Buy low, sell high'.
Through identifying the most relevant variables which could improve price, we decided to focus on those which could easily be
changed for the better
These were:
a) Small houses on large lots, where expansions can be built more easily. The small house/large lot was also demonstrably 
cheaper to purchase
b) Structural improvements such as bathrooms and bedrooms, both of which show an improvment in price with greater numbers
c) Cosmetic improvements to the property's condition, the largest jumps of which were from level 2 - 3 (on the condition index)
Through identifying these variables had a useful focus on which to build our analysis of price prediction from potential
improvements to a property which fulfills the above requirements.

DATA CLEANING AND EDA

The approach to data cleaning was to pick up on missing variables initially, then recognise outliers. Once the missing
variables were removed, through utilisation of the pandas null value command and suitably substituted through using the 
mode of the columns, we were able to plot graphs with the total values of the columns, minus the missing values.
We then decided to remove the outlier values to create our final plots of data. This was to exclude the largest, and most 
expensive properties, as this did not fit our business model. We thereby created different visualisations to further get
across the value of our data analysis and potential price predictions. 

REGRESSION MODELS

Overall, four regression models were built:


The first model used all sought to identify the variables that most impact the price of the property. This model used the variables highlighted as having the greatest correlation with price in the Exploratory stage and included:


a) sqft_living15


b) bathrooms  


c) grade


This returned a R-squared of 0.46 with sqft_living15 contributing the greatest.


The second model sought to answer the question: Which structural features make the largest impact on price? And included the variables bathrooms, yrs_since_renovation, and bedrooms.
This returned a R-squared of 0.2 with bathrooms contributing the greatest.


The third model sought to answer the question: How much impact does cosmetic condition have on price? And included the variables condition and yrs_since_renovation
This returned a R-squared of only 0.02 and was therefore dismissed.


The fourth model sought to answer the question: Are higher prices associated with larger properties, larger land or both? And included the variables sqft_living and sqft_lot
This returned a R-squared of only 0.39 with sqft_living being the main contributor.
