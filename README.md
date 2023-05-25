# Machine_learning_happiness3
Master: Sustainable management and Technology, at IMD, EPFL, HEC-UNIL.

Course: "Data science and Machine learning", second semester.

Authors: Sofia Estero, Lorenzo Parma, Siméon ...

This read.me provides an overview on the project, a more detailed content can be found in the assignment notebook. 

## Introduction
This research seeks to quantitatively analyze the factors that influence varying levels of happiness across countries. To achieve this, the study will commence with a brief review of recent literature and will then build upon these insights by analyzing the 2016 world metrics dataset. This dataset includes data from reputable sources such as the World Health Organization, Global Ecological Footprint, Human Freedom Index, and World Happiness Report. The paper performs an analysis of the data and tries to build different models with the aim of predicting the value of happiness according to the variables provided by the dataset, in particular: linear and polynomial regression, Support Vector Regressor, Gradient Boosting, Decision tree, Random Forest and Neural Network. In the last chapter the results of these model are compared and evaluated according to three main metrics: MAE; MSE and RMSE. 

## Literature Review
To align this work with curriculum of the MSc Sustainable Management & Technology (of which the authors are part of), this paper will analyze the relationship between happiness and SDGs across countries. While the SDGs do not explicitly mention happiness as a goal or target, many of the goals are directly related to promoting well-being and elevating societies. An important work from Iriarte (2022) shows a positive correlation between subjective well-being, SDGs index, and environmental indicators. The author discusses the need to decouple well-being levels from consumption levels and promote more conscious societies by encouraging intrinsic values and mindfulness.
The aim of promoting sustainable development is to enhance the standard of living for individuals across the globe (Aksoi & Arli, 2019). In their study, the reveal that happiness is positively correlated with the environmental dimension of sustainable development and that enhancing social sustainability has a positive impact on happiness. However, no statistically significant correlations were found between the economic dimension and happiness. A deeper discussion of other papers related to the relationship between happiness and sustainability can be found in the notebook. 

As far as the variables that mainly affect happiness are concerned, the World World Happiness Report (WHR) is presented in the notebook. It identifies several factors that contribute to global declines in happiness, including the COVID-19 pandemic, climate change, and economic inequality. Nonetheless, another article published in the Journal of Community Psychology identifies social justice as the second predictor of people's happiness, following social capital. 
Similarly, in this instance, as previously mentioned, a deeper analysis of the topic is provided in the literature review of the notebook. 

## Clustering analysis
After checking the cleanness od the data and performing a dependent variable exploration, a clustering analysis was conducted. In this regard, we used KMEANS and Hierarchical Clustering. In the dependent variable exploration it was discovered that Ecological footprint has a moderate, positive correlation with happiness. In light of this, we clustered countries based on levels of happiness and ecology and we analyzed the geographical relationship between the two.


## Regression analysis
First, it was necessary to classify our research question. Indeed, happiness is measured on a continuous scale, entailing that the problem faced is an instance of a regression problem. In this regard, we also defined the metrics used to evaluate our models, that are: R2, MAE, MSE and RMSE, describing the reasons ceiled behind the choice of these measures. Consequently, all the models are applied, commencing with a baseline algorithm exemplified by Linear Regression, and progressing to gradient boosting, support vector regression, decision tree, random forest, until Neural Networks. For each of the examined models, we endeavored to enhance their performance by implementing optimized parameters or by applying regularization techniques. The result of each model was systematically reported in a common table which, progressively, summarized all the tests conducted, which is represented below.

<img width="809" alt="Schermata 2023-05-25 alle 14 37 50" src="https://github.com/sofiaestero/Machine_learning_happiness3/assets/114024000/b163fcc7-9ba0-4c2d-af3d-669733eaad86">


## Discussion



# Conclusion

