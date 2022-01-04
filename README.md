# Methods to handle with missing data

This project aims to demonstrate some data pre-processing techniques when we have a missing data problem. The techniques presented were used in real data.

## Problem Description and Objectives:

High concentrations of certain harmful algae in rivers constitute a serious ecological problem with a strong
impact not only on the life forms of rivers, but also on the
water quality. Being able to monitor and carry out a
Early prediction of harmful algae is essential to improve
the quality of rivers.

In order to solve this prediction problem, several water samples were collected from different European rivers at different times during a period of
approximately 1 year. For each water sample, different chemical properties were measured, as well as the frequency of occurrence of seven harmful algae.

Some other features of the water collection process
were also stored, as the season of the year, the
river size and river velocity. One of the main
motivations behind this application lies in the fact that
chemical monitoring is cheap and easily automated,
while the biological analysis of the samples to identify the
algae that are present in the water involves examination
opic microscopy, requires trained labor and is therefore expensive
is slow. 

As such, obtaining models that are capable of predicting
algae frequencies based on chemical properties
would facilitate the creation of cheap and automated systems for
monitoring of harmful algae.

## Data

Each observation contains information about 11 variables, three
of these variables are nominal and describe the season of the year 
in which the water samples to be aggregated were
collected, as well as the size and speed of the river in
question. The remaining eight variables are values ​​of different
parameters measured in the water samples.

## The methods used are:

1. Missing data deletion method
2. Average value method
3. Correlation and linear regression
4. Nearest neighbors method
5. Predictive Mean Matching Method

Let's talk about each method carefully.

## Missing data deletion method

As the name says, it's just the deletion of all missing data. It is the simplest method, but in some situations it may have some problems because the missing data can be of fundamental importance for future data analysis.

## Average value method

It is a method based on replacing the missing data with the mean, mode or median. The most important question is:

### When to use the mean or median?

1. If the distribution is approximately normal, where the
observations are well grouped around the mean, the mean must be selected.
2. For asymmetric distributions, with many outliers, the
median and a more robust measure to be imputed.
3. In case the variable is nominal, the mode is selected

## Correlation and linear regression

This method is used by exploring the correlation between variables, and then using
single or multiple linear regression with complete data
to impute with the response variable as the variable
with missing data.

## Nearest neighbors method

It is verified for each observation with missing data which the
nearest neighbor, and is measured with the distance as the following:

![equation](https://github.com/AlbertoRodrigues/methods_missing_data/blob/main/images/ex1.png)

Then it can be used from the k closest neighbors to
median of the variable with missing data or an average
weighted by the exponential kernel function

## Predictive Mean Matching Method

Method that uses multiple linear regression, k nearest neighbors and the regression estimator to estimate missing data.


# The notebook jupyter used to apply all these techniques is [here](https://github.com/AlbertoRodrigues/methods_missing_data/blob/main/methods_missing_data.ipynb)
