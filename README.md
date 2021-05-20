# Global Happiness Data Analysis and Prediction

Data: Kaggle - https://www.kaggle.com/unsdsn/world-happiness

## Project Description
This was my very first data science project for a data scince course I took in 2018. My goal was to examine what factors contribute to a society's happiness, how those factors relate, and which are the most important in predicting happiness or overall quality of living. 

## Data Overview
The data measures the overall happiness of people groups in 157 countries (9 regions)
Scores 7 factors: Economy, Family, Life Expectancy, Freedom, Trust (government), Generosity, and Dystopia residual (dystopia refers to  a society characterized by human misery or oppression).

Categorical variables:
* Country
* Region

Numeric variables:
* Economy
* Family
* Life Span
* Freedom
* Government Trust
* Generosity
* Dystopia Residual
* Happiness Score - sum of scores for all 7 factors
* Happiness Rank - rank given to each country based on happiness score (1 being the highest rank)

\
Summary of numeric variables
![Screen Shot 2021-05-20 at 2 50 22 PM](https://user-images.githubusercontent.com/54850909/119040250-c956f500-b97a-11eb-907e-42e996b32c8a.png)

At the time of this analysys, data was available up to 2017. The 2017 data, however, did not include Region. Because I was interested in using Region in this analysis, I decidd not to include the 2017 data in my final data frame. 

## Exploratory and Visual Analysis
Happiness score by region
![Screen Shot 2021-05-20 at 2 57 50 PM](https://user-images.githubusercontent.com/54850909/119041065-c7416600-b97b-11eb-896d-8fcfd9bb62c0.png)
\
Note that this rank is based on only two years of data and may vary significantly from year to year.

Correlations
![Screen Shot 2021-05-20 at 2 59 36 PM](https://user-images.githubusercontent.com/54850909/119041253-040d5d00-b97c-11eb-809d-5f37043e35fd.png)
\
Heatmap - visual representation of correlations \
![Screen Shot 2021-05-20 at 2 58 55 PM](https://user-images.githubusercontent.com/54850909/119041181-ea6c1580-b97b-11eb-88db-5f5198df8e89.png)
\
In this heatmap, lightest colors show positive correlations between variables and darkest colors show negative correlations between variables. My goal was to examine the relationships between these variables and use them to predict the happiness score.


