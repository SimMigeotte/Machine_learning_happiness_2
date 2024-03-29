# Machine_learning_happiness_02
Master: Sustainable Management and Technology, at IMD, EPFL, HEC-UNIL.

Course: "Data science and Machine learning", second semester 2022/2023.

Authors: Sofia Estero, Lorenzo Parma, Siméon Migeotte.

Youtube  video: https://www.youtube.com/watch?v=t3avFaiXLng&feature=youtu.be&ab_channel=SofiaEstero

This read.me provides an overview on the project, outlining the description and the main results. A more detailed content can be found in the assignment notebook. 

## Introduction
This paper aims to uncover common patterns of happiness among countries and develop accurate Machine Learning algorithms for predicting a country's happiness score. It begins with a review of recent literature and analyzes the 2016 world metrics dataset, which includes data from reputable sources. Various models, including linear regression, polynomial regression, Support Vector Regressor, Gradient Boosting, Decision tree, Random Forest, and Neural Network, are built to predict happiness values. The results are evaluated based on metrics such as MAE, MSE, and RMSE in the final chapter. This study aims to fill a research gap by examining the relationship between happiness and sustainability through a clustetering analysis. The regression part that follows shed light into the validty of algorithms in the scope of the current project.

## Literature Review
To align with the curriculum of the MSc Sustainable Management & Technology program, the literature review of this research paper explores the relationship between happiness and the Sustainable Development Goals (SDGs) across countries, particularly those relating to the environmental protection. Although the SDGs do not explicitly mention happiness, many goals are directly linked to promoting well-being and societal upliftment. Previous studies have shown a positive correlation between subjective well-being, the SDGs index, and environmental indicators. The objective of sustainable development is to enhance the global standard of living, with happiness being positively associated with the environmental dimension of sustainability. Factors affecting happiness, such as the impact of the COVID-19 pandemic, climate change, and economic inequality, are discussed in the World Happiness Report and other relevant literature sources. For a more comprehensive analysis of the relationship between happiness and sustainability, please refer to the accompanying documentation.

## Clustering analysis
After checking the cleanness of the data and performing some variables exploration and visualization, a clustering analysis was conducted. In light of the positive correlation between Ecological footprint and happiness discovered during the dependent variable exploration, we clustered countries based on levels of happiness and ecology and we analyzed the geographical relationship between the two. Through the testing of K-means and hierarchical clustering algorithms, we have found that the 5 clusters generated by K-means provide a more comprehensive depiction of regional disparities in happiness and ecological scores compared to the 3 clusters produced by the hierarchical algorithm. By incorporating a greater number of clusters, we can capture the nuanced variations within regions and gain a better understanding of the interplay between happiness, ecological scores, and geographical factors. From the analysis, we concluded that African countries are associated with lower happiness levels and lower emissions. Western countries show higher happiness levels and environmental footprints, with Scandinavian countries being an exception with low emissions. Nevertheless, clusters are subjective and caution is needed in interpreting them. Here is the map that was returned by the 5 clusters of Kmeans:

![clusters](https://github.com/sofiaestero/Machine_learning_happiness3/assets/114024000/1b1d8685-ddb6-4ec6-bb1c-b6d7862568a6)


## Regression analysis
The measurement of happiness on a continuous scale necessitates treating the problem as a regression task. In this study, we have defined specific metrics to evaluate the performance of our models, namely R2 (coefficient of determination), MAE (mean absolute error), MSE (mean squared error), and RMSE (root mean squared error). These metrics were selected based on their ability to capture different aspects of model performance, taking into account both the accuracy and precision of the predictions.  Subsequently, a range of models was employed, starting with a baseline algorithm such as Linear Regression, and progressing to more advanced techniques including gradient boosting, support vector regression, decision tree, random forest, and ultimately Neural Networks. In order to improve the performance of each model, we explored parameter optimization and utilized regularization techniques where applicable. The findings from each model were consistently recorded and summarized in a comprehensive table, which is presented below, providing a concise overview of all the conducted tests.

<img width="1201" alt="Schermata 2023-06-03 alle 18 35 56" src="https://github.com/sofiaestero/Machine_learning_happiness3/assets/114024000/f4bf168d-d107-401a-bf5d-c8f1ed5e7c56">

We provide a detailed ranking for each evaluation metric in the notebook, with clear explanations of the results and an extensive discussion on the findings. Here, we report the most important considerations:
- Hyperparameter tuning proved successfull across models.
- According to the MAE metric, the Neural Network Optimized approach demonstrates the best performance, with a remarkably low value of 0.4196.
- The Neural Network Optimized model achieved the lowest MSE of 0.2537, indicating minimal squared deviations between its predictions and the actual happiness values. Lasso and Ridge regularization techniques also demonstrated solid performance.
- The lowest RMSE on the test set is again achieved by the Neural Network Optimized, with a value of 0.5037. This indicates that the model's predictions exhibit minimal deviations from the actual happiness values. Similar conclusions as above for LASSO and Ridge. 

## Discussion
In the clustering analysis, we have taken great care to prioritize both environmental sustainability and overall happiness. We emphasize that there isn't necessarily a conflict between being an environmentally conscious country and experiencing widespread happiness. These two aspects can complement each other. However, significant government intervention is necessary in various aspects of society, and it is crucial for nations, regardless of their political affiliations, to prioritize the Sustainable Development Goals (SDGs) as a central part of their agenda.

For the regression problem, NN has shown to outperform other models in all the metrics considered. NN models have the ability to capture complex non-linear relationships between input features and target variables, which characterize the patterns of the current happiness research question. Nonetheless, NN models are also capable of automatically extracting relevant features from the input data. This alleviates the need for manual feature engineering, which can be a challenging and time-consuming process as NN models demonstrated, in this case, relatively shorter training and running times compared to other complex models. Furthermore, it is noteworthy to underline that the Lasso and Ridge regularization techniques, which were quite simple to implement, exhibited the second and third lowest errors among all the metrics examined. This finding is encouraging as it indicates their suitability for addressing the research question at hand without requiring advanced machine learning expertise to deploy.
It is necessary to recognize that the dataset used in this study was relatively small, clean and it did not suffer from the problem of high dimensionality. With a larger number of features and potentially more complex relationships to capture, the training and running time of NN models may be affected. Therefore, testing the models on datasets with more features and potentially longitudinal data can provide insights into the scalability and robustness of NN models.


# Conclusion
In the present study, we conducted an exploratory data analysis comprising data visualization, clustering, and regression analysis to examine the intricate relationship between country-specific characteristics and happiness. Clustering techniques were employed to categorize countries based on their happiness and ecological scores. 
Following the analysis, a thorough evaluation of multiple regression algorithms was conducted to predict happiness scores based on our dataset. Remarkably, our Neural Network model exhibited outstanding performance in accurately forecasting happiness scores, closely followed by a linear regression model incorporating regularization techniques like Lasso and Ridge. It is worth mentioning that the characteristics of the current dataset enabled us to achieve satisfactory results within a reasonable running time. Future research should explore the performance of the analyzed models on larger datasets to further validate their effectiveness.





