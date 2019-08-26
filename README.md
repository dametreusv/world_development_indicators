# Predicting Income Groups Using World Development Indicators

For full report click [here](https://github.com/dametreusv/world_development_indicators/blob/master/WDI_final_report_.ipynb)

To download the datasets click [here](https://datacatalog.worldbank.org/dataset/world-development-indicators).

<img src="https://github.com/dametreusv/world_development_indicators/blob/master/images/modeling_spider_scores2.png" width="450" height='450'>


## Table of Contents
--------------------------

### Introduction
[About the World Bank & World Development Indicators](http://datatopics.worldbank.org/world-development-indicators/)

[The Proposal](https://github.com/dametreusv/world_development_indicators/blob/master/WDI_proposal.pdf)

[The Datasets](https://datacatalog.worldbank.org/dataset/world-development-indicators)


### Data Wrangling

[Data Acquistion and Cleaning](https://github.com/dametreusv/world_development_indicators/blob/master/WDI_wrangle.ipynb)


### Exploratory Data Analysis

[Data Analysis](https://github.com/dametreusv/world_development_indicators/blob/master/WDI_analysis.ipynb)

- [Data Analysis with Internal Navigation Links](https://nbviewer.jupyter.org/github/dametreusv/world_development_indicators/blob/master/WDI_analysis.ipynb)


### Milestone Report
[Report via Github](https://github.com/dametreusv/world_development_indicators/blob/master/WDI_milestone_report.ipynb)

- [Report with Internal Navigation Links](https://nbviewer.jupyter.org/github/dametreusv/world_development_indicators/blob/master/WDI_milestone_report.ipynb)


### Machine Learning Modeling
[ML Preparation & Modeling](https://github.com/dametreusv/world_development_indicators/blob/master/WDA_modeling.ipynb)

- [ML Preparation & Modeling with Internal Navigation Links](https://nbviewer.jupyter.org/github/dametreusv/world_development_indicators/blob/master/WDA_modeling.ipynb)


### Final Report
[Predicting Income Groups Using World Development Indicators](https://github.com/dametreusv/world_development_indicators/blob/master/WDI_final_report_.ipynb)


## Executive Summary

Through analysis, we have found that:
- Countries change income groups from year to year
- Higher income groups are growing while lower income groups are shrinking.
- Features are showing a growth in access and standards of living among all income groups.
- This all leads to the world becoming more developed.


The major indicator that determines income group is GNI per capita.  Countries fall into certain groups based off of this feature, which is also correlated to many world development indicators and is worth a deep dive.

In analyzing our data, we were able to separate our features into various categories:
- Economic Policy and Debt
- Education and Gender Issues
- Access to Advanced Communications
- Environment, Resources and Population
- Social Protection and Labor
- Health

We are looking to predict the economic standing of countries using world development so we dropped features that pertained to GNI and GDP. Feature selection is an important process to reduce training time and defend against overfitting. In selecting features, we used an anova based univariate method and also a tree based method. We were able to obtain a combination of 37, 25, 17 and 8 features to use when training our models.

In training and testing our models, we created a pipeline that would simulate every feature and hyperparameter combination using a 5 fold cross validation method in order to give us the best method that we would test on unseen data and re-tune according to performance. Our models performed extremely well in predicting high income groups and really well in predicting low income groups. The models started to dip in accuracy, precision and recall as they attempted to predict upper and lower middle income groups. The model that performed the best was the random forest model, using only 17 features to predict income groups. This model had an accuracy, precision, recall and f1-score of just under 94%. What really set the model apart from all other models was its ability to be exremely precise in predicting low income groups, predicting 177 out of 178 correctly.

<img src="https://github.com/dametreusv/world_development_indicators/blob/master/images/milestone_Life%20expectancy%20at%20birth%2C%20total%20(years)_1.png?raw=true">
<img src='https://github.com/dametreusv/world_development_indicators/blob/master/images/model_GNI_Intersection_of_Income_Groups.png?raw=true'

<img src='https://github.com/dametreusv/world_development_indicators/blob/master/images/modeling_spider_scores2.png?raw=true'  width='500'>

<img src='https://github.com/dametreusv/world_development_indicators/blob/master/images/modeling_scores.png?raw=true' width='1000'>

<img src='https://github.com/dametreusv/world_development_indicators/blob/master/images/modeling_random_forest.png?raw=true' width='700'>
