# Methods for handling missing data

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

!(equation)[https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D%20d(%5Ctextbf%7Bx,y%7D)=%20%5Csqrt%7B%5Csum_%7Bi=1%7D%5E%7Bp-a%7D%5Cdelta_%7Bi%7D(x_%7Bi%7D,y_%7Bi%7D)%7D%5C%5C%5Ctext%7Bwhere%20%7D%5Cdelta_i=%20%5Cbegin%7Bcases%7D1%20&%20%5Ctext%7B%20if%20both%20variables%20are%20categorical%20and%20%7D%20x_%7Bi%7D=y_%7Bi%7D%20%20%5C%5C%200%20&%20%5Ctext%7B%20if%20both%20variables%20are%20categorical%20and%20%7D%20x_%7Bi%7D%20%5Cneq%20y_%7Bi%7D%20%5C%5C%20(x_%7Bi%7D-y_%7Bi%7D)%5E2%20&%20%5Ctext%7B%20if%20both%20variables%20are%20numeric%7D%5Cend%7Bcases%7D]




