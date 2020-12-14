# GSHAP

The GSHAP module is a direct extension to Scott Lundberg and Su-In Lee's [kernel Shap](https://github.com/slundberg/shap/blob/master/shap/explainers/_kernel.py).

The GSHAP module computes global SHAP values, based on the approach used by Scott Lundberg and Su-In Lee in their paper ["A Unified Approach to Interpreting Model Predictions"](https://arxiv.org/abs/1705.07874).

The GSHAP method uses the [kernel SHAP](https://github.com/slundberg/shap/blob/master/shap/explainers/_kernel.py) method, in order to compute global SHAP values. The benefit herein is, the computation of **global** SHAP values in common and thereby *comparable* units. Thus there is no need of scaling the features, to make global feature contribution measures comparable. These are in the unit of a score measure specified by the user. The choices are:

- accuracy score
- recall score
- precision score
- area under the roc score

This score can be used for model selection, in order to improve the model with respect to a certain score measure.
