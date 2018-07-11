Yet Another Information Criterion
=================================

This package implements methods from 
the papers *Post-selection inference: estimation of leverage
and squared error optimism via flows* and [*Degrees of freedom for piecewise 
Lipschitz estimators*](https://projecteuclid.org/euclid.aihp/1524643230) by 
Frederik Vissing (formerly Riis) Mikkelsen and Niels Richard Hansen. 

These papers develop valid estimates of *covariance penalties* 
after model selection, which quantify leverage of individual observations
as well as the total optimism of the training squared error. The 
resulting information criterion (YAIC) is an approximately unbiased estimate
of mean squared error. This should be contrasted to AIC, Mallows's Cp 
and SURE that do not correctly account for model selection and are 
thus overly optimistic, just as classical leverage quantities underestimate 
the influence of individual observations when model selection is used.

YAIC is based on properties of the model 
selection algorithm as a function of one or more tuning parameters that 
allow for direct estimation of covariance penalties. Alternatives for 
estimating covariance penalties include bootstrapping and leave-one-out 
cross-validation. Compared to these methods, YAIC
has a small computational overhead on top of the computation 
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
