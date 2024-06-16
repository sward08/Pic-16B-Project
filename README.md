# Pic-16B-Project

**Project Summary:**
The “Insurance Dataset for Predicting Health Insurance Premiums in the US” from Kaggle is a comprehensive collection of data designed to explore factors affecting medical costs and health insurance premiums in the United States. 

**Primarily, our goals with the dataset are to:**
Explore and visualize the correlations between various factors that could affect health premiums
Find the best model that would be able to predict insurance charges for individuals based on important features from the dataset.

**Models and their Peformance:**
- K-NN
a. MSE: 1.6
B. R2: 0.91

- Linear Regression
a. MSE: 0.13
b. R2: 0.99

- SVR
a. MSE: 0.15
b. R2: 0.99

- Neural Network
a. MSE: 0.211

- Cluster Linear Regression
a. Cluster 0:
MSE: 0.089
R2: 0.995
b. Cluster 1:
MSE: 0.083
R2: 0.996

**Conclusion:**
Before, our best model as reflected by the scores was linear regression but in comparison, this new model scored better. This also makes sense because clustered linear regression is supposed to improve the accuracy of normal linear regression which is exactly what was reflected in our CLR model.

After further analysis by examining cluster centroids, we found that we could possibly predict what features are contributing to our clusters:
Cluster 0: This cluster might represent younger individuals with slightly lower BMI, fewer children, a higher proportion of smokers, more people who never or occasionally exercise, slightly more blue-collar workers and unemployed individuals, and a higher proportion of people with Premium coverage.
Cluster 1: This cluster might represent older individuals with slightly higher BMI, more children, a lower proportion of smokers, more people who exercise rarely, slightly more students and white-collar workers, and a higher proportion of people with Standard coverage.

By analyzing these centroids, we can infer that Cluster 0 tends to consist of younger, possibly single individuals or couples without children, with slightly higher smoking rates and are receiving higher insurance coverage. Cluster 1 tends to consist of older individuals, possibly families with children, with slightly lower smoking rates, and are receiving Standard coverage.

These interpretations are useful when trying to predict health premiums and insurance charges.

Relationships between categorical variables and charges:
Region does not have a large effect on charges. Regardless of whether the individual is from the southeast, northeast, southwest or the northwest, charges are relatively consistent.
Gender does not have a large effect on charges. However, males have a slightly larger insurance charge than females.
Smokers have significantly higher charges when compared to non-smokers
People with no recorded medical history have the lowest charges, followed by those with high blood pressure, then diabetes. Those with heart disease histories have the highest charges. The same pattern is true for family medical history.
Unemployed individuals and students have relatively similar charges, whereas people with white and blue collar occupations have relatively higher charges.


**PIC 16B Project Proposal**
Group: Dakota Lin, Anshika Khandelwal, Sarah Ward

Describe what problem the project addresses, the relation between your project and your background or major, and why you are interested in this project. 

The project aims to address the unpredictability of insurance premiums for individuals. In today's dynamic insurance market, individuals often face uncertainty regarding whether the premiums they pay accurately reflect their health risks. For insurance companies, inaccurately assessing consumer risk and selling inappropriate insurance packages can result in substantial losses. This problem underscores the critical need for a deeper understanding of the factors influencing insurance premiums and effective risk assessment strategies.

As students majoring in Applied Mathematics and Economics, this project aligns with our academic background. For instance, economics provides insights into the broader economic implications of insurance pricing and risk assessment. Concepts relevant in Economics, such as adverse selection, where purchasers possess more information about their risk than insurers, are particularly relevant in understanding the challenges insurers face in accurately pricing insurance packages. 

Our interest in the topic stems from a necessity: after all, everyone requires health insurance. This project will be useful in choosing which health insurance coverage fits with our lifestyle the best. Overall, this project aims to not only predict the effect of various factors on charges, but also classify which premiums the individual is in.

Describe what resources, such as data, computing power, and etc, you need in order to complete your project. Please pay special attention to the question of data. If your project idea involves data, include at least one link to a data set you can use. It’s also acceptable to link to a website from which you intend to scrape the data you will use (although note that high-quality scraping is a lot of work).  

We will use this Kaggle dataset for predicting health insurance premiums in the US as our primary data for the project. This dataset contains a mix of categorical and numerical individual attributes that can be used as informative features for predicting their coverage levels and charges. 

Applications running on the entire dataset will consume extremely demanding computing power, as there are 1 million rows, so we may randomly extract a subset to base our analysis on.

Summarise previous work related to your project. For example, if you want to do a data science project using dataset from Kaggle, you should summarize other's work (models, prediction error, and etc. ) 

Medical charges estimation
Sample: subset of 2,000 samples out of 1,000,000
Models: Linear regression and Multi linear regression
Conclusions: 80% accuracy achieved in predicting charges

This is currently the only complete code for this dataset on Kaggle. Although it does apply regression models which we also attempt to use, we aim to further extend it by improving the accuracy as well as exploring the classification models.

Describe required tools and skills.

We will first implement the fundamental data preprocessing steps using packages like pandas and numpy to prepare the data for model training. Then we will import the supervised machine learning models from libraries like scikit-learn to fit the training set and predict the target variables while quantifying the feature contributions. In addition, we will use the plotting tools including Plotly and Networkx to visualize various results, like the description statistics of the dataset and the correlation between different features and target. We also need to import the evaluation metrics to assess and compare the performance of different models, like the confusion matrices, F1 accuracy scores, etc. 

Furthermore, we also want to experiment on a possible approach, which is to build a similarity network to categorize patients based on health profiles and set benchmarks for coverage charges of different plans. This could be done using one-hot encoding, cosine similarity, and clustering algorithms involving topic modeling. Evaluation metrics for clusterings without ground truths like silhouette coefficient and Davies Bouldin score can be used here. 

Describe what you will learn.

From this project, we will learn several key aspects related to health insurance and predictive modeling:
Understanding the Relationship Between Health Insurance Plan Choices and Health Attributes: by exploring the relationship between individuals' health insurance plan choices and their health attributes, we will gain insights into the factors that influence insurance plan selection. This analysis will help us understand how individuals' health profiles, such as medical history, lifestyle choices, and demographic factors, influence their preferences for certain insurance plans.
Building an Effective Model for Recommending Insurance Plan Choices: developing a model that recommends insurance plan choices based on individuals' health profiles will require us to employ machine learning techniques such as classification algorithms. By training the model on archived data, we will learn how to effectively analyze and process health data to make personalized recommendations. 
Predicting Health Insurance Costs Based on Various Factors: predicting an individual's health insurance costs will involve building regression models that consider various factors such as age, gender, health attributes, coverage plan choices, and possibly regional factors. By training regression models on historical data, we will learn how to quantify the impact of different variables on insurance costs and how to make accurate predictions for new individuals.

Include group members and role and tentative timeline for each group member.

<img width="750" alt="Screenshot 2024-04-30 at 5 59 16 PM" src="https://github.com/sward08/Pic-16B-Project/assets/130085359/640972e4-1fb2-4582-b06c-3f7ffaf959a5">


