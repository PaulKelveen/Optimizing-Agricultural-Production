Optmizing Agricultural Production Machine Learning Project

Project Description

Historically, agricultural practices were informed primarily by the empirical knowledge and hands-on expertise of farmers. However, the adverse impacts of climate change on crop yields have become increasingly apparent. Consequently, farmers face challenges in making informed decisions regarding crop selection based on soil and environmental factors. Manual methods of predicting suitable crops for a given piece of land often prove ineffective. The integration of machine learning has emerged as a pivotal solution in the realm of crop prediction, with the outcome significantly influencing crop production. The accuracy of crop prediction hinges upon the consideration of soil composition and climatic conditions.

This project is focused on training a supervised machine learning model using Logistic Regression on existing soil and climatic conditions to predict the optimum crop to be planted based on any given soil and climatic condition.

Introduction

In the context of a nation's development, a critical determinant is its capacity for efficient food production. Throughout successive generations, the cultivation of essential food crops has been integrally linked to the agricultural sector. However, a contemporary concern of paramount significance is the unprecedented rate of population growth. This demographic surge has exerted a notable impact on the agricultural landscape, particularly in terms of land utilization and fertility. Given the constraints posed by urbanization and globalization, the feasibility of expanding cultivated land is constrained. Accordingly, there exists a compelling need to strategically optimize extant resources.

Predicting suitable crop for cultivation is an essential part of agriculture, with machine learning algorithms playing a major role in such prediction in recent years. In this era of technology and data science, the agricultural sector stands to benefit greatly from properly implemented techniques.

Dataset

This project utilized an agricultural dataset that is open to the public and collected from Kaggle's website. The dataset contains 8 attributes or columns : 4 of which are related to the soil composition, 3 columns are related to climatic conditions and 1 columns for the label or target variable. The dataset also contains 2200 instances or rows. The label or target variable contains 22 distinct classes.

Libraries used for analysis
Python is primarily used for the project and the following variables were used in importing, exploring, visualizing and analysing the dataset.
-NumPy
-Pandas
-Seaborn
-Matplotlib
-Sklearn
-Ipywidgets
-Tableau

Exploratory Data Analysis

    -As earlier highlighted, this dataset contains 2200 rows and 8 columns. The column names in this dataset is as follows: Nitrogen (N), Phosphorus (P), Potassium (K), Ph, Temperature, Humidity and Rainfall.
-7 of the 8 columns are numerical columns except for the target or label column.
    -The data set does not contain any missing values.
    -Using box plots to visualize the dataset, it can be observed that there seems to be lots of data points that at first glance, looks like "outliers" for all of the factors except nitrogen. However, upon further examination, this is due to the different optimal soil conditions for the different plants.
    -Each unique crop or distinct class of the target variable has 100 rows of data, representing 4.5% of the entire data set.
    -The summary statistics for the dataset:
        --Average Ratio of Nitrogen in the Soil: 50.55
        --Average Ratio of Phosphorus in the Soil: 53.36
        --Average Ratio of Potassium in the Soil: 48.15
        --Average PH Value of the Soil: 6.47
        --Average Temperature in Celsius: 25.62
        --Average Relative Humidity in %: 71.48
        --Average Rainfall in mm: 103.46
    -We also discover the following facts:
        --Cotton requires a very high ratio of nitrogen content in the soil.
        --Grapes and Apples requires a very high ratio of phosphorus and potassium content in the soil.
        --Most crops require a ph level between 6 and 7
        --Most crops require temperatures above 20C with Papaya and Grapes needing the highest temperatures at above 30C.
        --Chickpea and Kidneabeans require the least humidity, around 20
        --Muskmelon requires the lowest rainfall at 25mm while rice has the highest at almost 250mm.


Findings

    -Using KMeans and the Elbow method, I found the optimal number of clusters in the dataset to be 4.
    -Therefore, this is the classification of the crops based on each cluster
        --Cluster 1
            ---Grapes
            ---Apple
        --Cluster 2
            ---Maize
            ---Chickpea
            ---Kidneybeans
            ---Pigeonpeas
            ---Mothbeans
            ---Mungbean
            ---Blackgram
            ---Lentil
            ---Pomegranate
            ---Mango
            ---Orange
            ---Papaya
            ---Coconut
        --Cluster 3
            ---Maize
            ---Banana
            ---Watermelon
            ---Muskmelon
            ---Papaya
            ---Cotton
            ---Coffee
        --Cluster 4
            ---Rice
            ---Pigeonpeas
            ---Papaya
            ---Coconut
            ---Jute
            ---Coffee
    -Logistic regression was used in the building of the model because it works better in the case of likelihood and multiple labels.

Model Accuracy and Results


Conclusion