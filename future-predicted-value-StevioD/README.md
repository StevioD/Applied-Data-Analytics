# Assignment: Predicting Future Value

One of the central metrics in a business-to-consumer (B2C) company is "Lifetime Value" (LTV), 
the amount that a given customer is expected to spend over the course of their shopping
with a company. Using a [MECE](https://en.wikipedia.org/wiki/MECE_principle) framework, we 
can divide LTV into past value and future predicted value (FPV). The past value is typically
pretty easy to determine. Predicting a customer's future value is much trickier and the 
focus of this assignment.

## Goals

Your goal is to predict FPV using the sales by owner, year, and month table from part three of the
Wedge project. Our data set ends in January 2017 and the Wedge was doing a remodel in 2016, which
depressed sales. Given those facts, we'll _predict spend by owner in 2015_ using _only_ data from 
before 2015. 

## Instructions

Build a linear regression model (or several models if you prefer) predicting spend in 2015 given
the data from before 2015. You'll have to do some data manipulation to prepare a data set 
for modeling. Turn in an RMD file and the knitted HTML. Write up your model indicating which 
terms are significant. After you have determined your model, split your data into "test" 
and "train" sets (I recommend a 10%/90% split or thereabout). Fit your model on your training
set and evaluate it on your test set. 

Calculate the [mean absolute percentage error](https://en.wikipedia.org/wiki/Mean_absolute_percentage_error)
on your predictions. If your estimate for FPV is `y_hat` and the true 2015 spend is `y`, then the MAPE is 
```
mean(abs(y_hat-y)/y)
```
I'd recommend plotting your errors (aka, residuals) on the test set to see where your errors tend to be.

Pay attention to the RMD and make sure your knitted document is an actual document, like you'd turn into
a class where you had an assignment to do a written report. This doesn't have to be long, but 
I'd like you to make it look semi-professional.


