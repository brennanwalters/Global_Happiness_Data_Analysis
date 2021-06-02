![Screen Shot 2021-05-24 at 8 09 24 PM](https://user-images.githubusercontent.com/54850909/119424896-f9c8c700-bccb-11eb-9b5d-84423ce95adc.png)

# Table of Contents
* Introduction
* Data Overview
* Analysis Results
* Prediction
* Conclusion

# Introduction
This was my very first data science project for a course I took in 2018. My goal was to examine which regions are the happiest, what factors contribute to a society's happiness, how those factors relate, and which are the most important in predicting happiness or overall quality of living. 

# Data Overview

Source: [Kaggle](https://www.kaggle.com/unsdsn/world-happiness)

Includes:
* Country (157 in total)
* Region (9 in total)
* The Happiness Score - the sum of numeric representations of the following factors:
  * Economy
  * Family
  * Life Span
  * Freedom
  * Government Trust
  * Generosity
  * Dystopia Residual (misery or oppression)
* Happiness Rank - rank given to each country based on happiness score (1 being the highest rank)

### Data collection 
According to the Content section of the Kaggle data description, "The happiness scores and rankings use data from the Gallup World Poll. The scores are based on answers to the main life evaluation question asked in the poll. This question, known as the Cantril ladder, asks respondents to think of a ladder with the best possible life for them being a 10 and the worst possible life being a 0 and to rate their own current lives on that scale."

### Summary
![Screen Shot 2021-05-20 at 2 50 22 PM](https://user-images.githubusercontent.com/54850909/119040250-c956f500-b97a-11eb-907e-42e996b32c8a.png)

At the time of this analysys, data was available up to 2017. The 2017 data, however, did not include Region. Because I was interested in using Region in this analysis, I decidd not to include the 2017 data in my final data frame. 

# Analysis Results

### Happiness score by region
![Screen Shot 2021-05-20 at 2 57 50 PM](https://user-images.githubusercontent.com/54850909/119041065-c7416600-b97b-11eb-896d-8fcfd9bb62c0.png)

* Australia and New Zealand had the highest overall happiness score
* Sub-Saharen Africa had the lowest overall happiness score
* Note that this rank is based on only two years of data and may vary significantly from year to year.

## Correlations
![Screen Shot 2021-05-20 at 2 59 36 PM](https://user-images.githubusercontent.com/54850909/119041253-040d5d00-b97c-11eb-809d-5f37043e35fd.png)


### Heatmap - visual representation of correlations
![Screen Shot 2021-05-20 at 2 58 55 PM](https://user-images.githubusercontent.com/54850909/119041181-ea6c1580-b97b-11eb-88db-5f5198df8e89.png)

In this heatmap, lightest colors show positive correlations between variables and darkest colors show negative correlations between variables. My goal was to examine the relationships between these variables and use them to predict the happiness score. Here we see that Economy, Family, and Life Span are most positively correlated with Happiness Score.

### Pairplot for Happiness Score, Family, Life Span, Generosity
![image](https://user-images.githubusercontent.com/54850909/119758211-c7ee6680-be6b-11eb-85c5-7c21bf45ddc1.png)

* As Family score increases, Happiness Score increases
* As Life Span score increases, Happiness Score increases
* Generosity not as impactful, no clear trend

### Pairplot for Happiness Score, Freedom, Economy, Government Trust
![image](https://user-images.githubusercontent.com/54850909/119758261-d9d00980-be6b-11eb-8850-4740c7ca3646.png)

* As Freedom score increases, Happiness Score also increases
* As Economy score increases, Happiness Score increases
* Government trust seems to have a non-linear relationship with Happiness Score

# Prediction
At the time of this analysis, I was very happy that both of the prediction models below had extremely high accuracies. I later realized that this was because Happiness Score is the sum of all the Family, Economy, Life Span, Generosity, Trust, Freedom, and Dystopia Residual scores. Thus, predicting Happiness Score based on these factors is not all that meaningful. Although I wish I had known this at the time, it still gave me valuable experience building prediction models.

### Training and Testing data
**Dependant variable:** Happiness Score \
**Factors:** Family, Economy, Life Span, Generosity, Trust, Freedom, Dystopia Residual

### Linear Regression
![Screen Shot 2021-05-26 at 10 02 19 PM](https://user-images.githubusercontent.com/54850909/119759567-1a308700-be6e-11eb-8099-db610f78fce7.png)

![image](https://user-images.githubusercontent.com/54850909/119759600-24528580-be6e-11eb-8f72-44c247d18891.png)

### K-Neighbors Regression

**Determine Best K value** \
![Screen Shot 2021-05-26 at 10 29 31 PM](https://user-images.githubusercontent.com/54850909/119761678-dccdf880-be71-11eb-99a2-86b069a2eb66.png)

![Screen Shot 2021-05-26 at 10 28 57 PM](https://user-images.githubusercontent.com/54850909/119761638-c7f16500-be71-11eb-8c77-88ca60bf6977.png)

Best value is K=3

![Screen Shot 2021-05-26 at 10 37 16 PM](https://user-images.githubusercontent.com/54850909/119762259-fa4f9200-be72-11eb-839a-128a17e1c24c.png)

Accuracy = 0.965

## Conclusion
* From the 2015 to 2016 data, I found that Australia and New Zealand had the highest overall happiness score and Sub-Saharen Africa had the lowest overall happiness score
* All of these factors contribute to a society's happiness
* Of the 7 factors, Economy, Family, and Life Span should be focused on when considering quality of human life.

