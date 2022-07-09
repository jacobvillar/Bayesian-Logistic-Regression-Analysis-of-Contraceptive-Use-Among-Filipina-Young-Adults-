# Bayesian-Logistic-Regression-Analysis-of-Contraceptive-Use-Among-Filipina-Young-Adults-

## **OBJECTIVES OF THE STUDY**
  The main objective of this study is to identify factors affecting the contraceptive use among young adults in the Philippines. Specifically, this study aims to:
  1. describe the distribution of contraceptive use among Filipina young adult characteristics,
  2. determine the association between contraceptive use and various socio-demographic characteristics of Filipina youth,
  3. construct a model that determines the factors associated with contraceptive use among Filipina young adults
  
## **DATA SOURCE**
  •Secondary data was utilized in this study. This quantitative analysis will make use of the requested dataset from the 2013 Young Adult Fertility and Sexuality (YAFS4) Survey conducted by the University of the Philippines Population Institute (UPPI) and the Demographic Research and Development Foundation (DRDF) in UP Diliman. 
  •It is a cross-sectional survey design 15-24 year-old Filipino youth nationwide and provides rich information on different aspects of a youth’s life, including reproductive health, sexual and non-sexual risk behaviors, societal relationships, education and labor, self-assessed well-being, among others (UPPI & DRDF, 2016).
  •In this study, the outcome variable is the history of contraceptive use with the subject’s partner or spouse. A female respondent is identified as a contraceptive user if she answered “yes” at the time of the survey. Otherwise, she is identified as a non-user. The independent variables used in the study were age, education, barangay stratum, ideal age for a woman to have her first child, marital status, and the poverty status of the respondent
  
## **DATA ANALYSES** 
  •The Bayesian approach for logistic regression analysis was used to fit a model that can predict if a given woman uses contraception. Following the study of Kana (2020) and Vehtari, Gabry and Goodrich (2017), this study estimated generalized linear models (GLMs) for binary Binomial response variables using the stan_glm function in the rstanarm package.
  •Corresponding posterior median estimates were extracted using the ‘coef’ function. In order to get a sense for the uncertainty of the estimate, the posterior_interval function was used to get the Bayesian uncertainty intervals. The 95% uncertainty intervals are computed by finding the relevant quantiles of the draws from the posterior distribution. In this study, a student t prior with 7 degrees of freedom and a scale of 2.5 were used. The stan_glm function returns the posterior distribution for the parameters describing the uncertainty related to unknown parameter values. 
  •In assessing the fit of the Bayesian logistic regression model, the ROC curve and confusion matrices were provided. Meanwhile, in measuring the predictive accuracy of the Bayesian model, cross validation was utilized. Specifically, the Pareto smoothed leave-one-out cross-validation (PSIS-LOO) wherein the expected log predictive density (elpd) was computed. 
