Yet Another Information Criterion
=================================

This package provides an implementation of methods developed in 
the papers *Post-selection inference: estimation of leverage
and mean squared error via flows* and [*Degrees of freedom for piecewise 
Lipschitz estimators*](https://projecteuclid.org/euclid.aihp/1524643230) by 
Frederik Vissing (formerly Riis) Mikkelsen and Niels Richard Hansen. 

These papers develop an information criterion (YAIC) that provide 
estimates of leverage for individual observations 
as well as global risk estimates that are valid after model selection. 
This should be contrasted to AIC, Mallows' Cp and SURE that do not
correctly account for model selection and are thus overly optimistic,
just as classical leverage quantities underestimate the influence 
of individual observations when model selection is used.

The information criterion is based on properties of the model 
selection algorithm as a function of one or more tuning parameters, and 
it provides direct estimates of *covariance penalties*. Alternatives for 
estimating covariance penalties include bootstrapping and leave-one-out 
cross-validation. Compared to these methods, YAIC
has a very small computational overhead on top of the computation 
of the regularization path of estimates parametrized by the tuning parameter. 

The package supports tuning parameter selection and model averaging (under
development) using YAIC for Gaussian linear regression models. Extensions
to generalized linear models is under development. 


## Installation

TODO

## Using the package

The package requires a model matrix and a vector of responses. Using 
one of the supported variable selection algorithms it returns an 
object with regression parameter estimates parametrized by the tuning 
parameter(s). 
