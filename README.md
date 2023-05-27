# Machine_learning_happiness3
Master: Sustainable management and Technology, at IMD, EPFL, HEC-UNIL.

Course: "Data science and Machine learning", second semester 2022/2023.

Authors: Sofia Estero, Lorenzo Parma, Siméon Migeotte

This read.me provides an overview on the project, a more detailed content can be found in the assignment notebook. 

## Introduction
This research seeks to quantitatively analyze the factors that influence varying levels of happiness across countries. To achieve this, the study will commence with a brief review of recent literature and will then build upon these insights by analyzing the 2016 world metrics dataset. This dataset includes data from reputable sources such as the World Health Organization, Global Ecological Footprint, Human Freedom Index, and World Happiness Report. The paper performs an analysis of the data and tries to build different models with the aim of predicting the value of happiness according to the variables provided by the dataset, in particular: linear and polynomial regression, Support Vector Regressor, Gradient Boosting, Decision tree, Random Forest and Neural Network. In the last chapter the results of these model are compared and evaluated according to three main metrics: MAE; MSE and RMSE. 

## Literature Review
To align this work with curriculum of the MSc Sustainable Management & Technology (of which the authors are part of), this paper will analyze the relationship between happiness and SDGs across countries. While the SDGs do not explicitly mention happiness as a goal or target, many of the goals are directly related to promoting well-being and elevating societies. An important work from Iriarte (2022) shows a positive correlation between subjective well-being, SDGs index, and environmental indicators. The author discusses the need to decouple well-being levels from consumption levels and promote more conscious societies by encouraging intrinsic values and mindfulness.
The aim of promoting sustainable development is to enhance the standard of living for individuals across the globe (Aksoi & Arli, 2019). In their study, the reveal that happiness is positively correlated with the environmental dimension of sustainable development and that enhancing social sustainability has a positive impact on happiness. However, no statistically significant correlations were found between the economic dimension and happiness. A deeper discussion of other papers related to the relationship between happiness and sustainability can be found in the notebook. 

As far as the variables that mainly affect happiness are concerned, the World World Happiness Report (WHR) is presented in the notebook. It identifies several factors that contribute to global declines in happiness, including the COVID-19 pandemic, climate change, and economic inequality. Nonetheless, another article published in the Journal of Community Psychology identifies social justice as the second predictor of people's happiness, following social capital. 
Similarly, in this instance, as previously mentioned, a deeper analysis of the topic is provided in the literature review of the notebook. 

## Clustering analysis
After checking the cleanness of the data and performing a dependent variable exploration, a clustering analysis was conducted. In this regard, we used KMEANS and Hierarchical Clustering. In light of the positive correlation between Ecological footprint and happiness discovered during the dependent variable exploration, we clustered countries based on levels of happiness and ecology and we analyzed the geographical relationship between the two.


## Regression analysis
First, it was necessary to classify our research question. Indeed, happiness is measured on a continuous scale, entailing that the problem faced is an instance of a regression problem. In this regard, we also defined the metrics used to evaluate our models, that are: R2, MAE, MSE and RMSE, describing the reasons ceiled behind the choice of these measures. Consequently, all the models are applied, commencing with a baseline algorithm exemplified by Linear Regression, and progressing to gradient boosting, support vector regression, decision tree, random forest, until Neural Networks. For each of the examined models, we endeavored to enhance their performance by implementing optimized parameters or by applying regularization techniques. The result of each model was systematically reported in a common table, which is also represented below, which summarizes all the tests conducted.

<img width="1059" alt="Schermata 2023-05-27 alle 00 36 12" src="https://github.com/sofiaestero/Machine_learning_happiness3/assets/114024000/279ce36a-48b8-4e9f-b34f-a65084164789">

We provide a detailed ranking for each evaluation metric in the notebook, here are we quote the most important considerations:
- The Neural Network Optimized model achieved the highest R2 score of 74.53% on the test set. Ridge and Lasso regularization techniques outperformed other nonparametric models, with R2 scores of 74% and 73.71% respectively. On the other hand, models based on 2 degrees polynomial regression lead to poor results with an R2 score of -84%. 
- Also according to the MAE metric, the Neural Network Optimized approach demonstrates the best performance, with a remarkably low value of 0.3773.
- The Neural Network Optimized model achieved the lowest MSE of 0.1883, indicating minimal squared deviations between its predictions and the actual happiness values. Lasso and Ridge regularization techniques also demonstrated solid performance.
- Lastly,the lowest RMSE on the test set is again achieved by the Neural Network Optimized, with an value of 0.4340. This indicates that the model's predictions exhibit minimal deviations from the actual happiness values. Similar conclusions as above for LASSO and Ridge. 

## Discussion
For the current problem, NN has shown to outperform other models in all the metrics considered. Indeed, NN models have the ability to capture complex non-linear relationships between input features and target variables, which characterize the patterns of the current happiness rresearch question. Nonetheless, NN models are also capable of automatically extracting relevant features from the input data. This alleviates the need for manual feature engineering, which can be a challenging and time-consuming process as NN models demonstrated, in this case, relatively shorter training and running times compared to other complex models. Furthermore, it is noteworthy that the Lasso and Ridge regularization techniques, known for their simplicity of implementation, exhibited the second and third lowest errors among all the metrics examined. This finding is encouraging as it indicates their suitability for addressing the research question at hand without requiring advanced machine learning expertise to deploy.
It is necessary to recognize that the dataset used in this study was relatively small, clean and it did not suffer from the problem of high dimensionality, with a larger number of features and potentially more complex relationships to capture, the training and running time of NN models may be affected. Therefore, testing the models on datasets with more features and potentially longitudinal data can provide insights into the scalability and robustness of NN models.


# Conclusion
In the present study, we conducted an exploratory data analysis comprising data visualization, clustering, and regression analysis to examine the intricate relationship between country-specific statistics and happiness. Clustering techniques were employed to categorize countries based on their happiness and ecological scores. 
Subsequently, a comprehensive assessment of various regression algorithms was performed to model the prediction of happiness scores using our dataset. Notably, a NN we built demonstrated exceptional performance in accurately forecasting happiness scores, followed by a polynomial regresson incorporating regularization techniques such as Lasso and Ridge. The caracteristics of the current dataset allowed us to achieve satisfactory results with a reasonable running time, however future research should explore the performance of the models analyzed on larger datasets. 
