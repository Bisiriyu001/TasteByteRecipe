# Recipe Popularity Prediction
Predicting High-Traffic Recipes for Homepage Recommendation

## Overview
This project builds a machine learning model that predicts whether a recipe will generate high website traffic when displayed on the homepage of a recipe platform. The business goal is clear. The product team wants to avoid missing popular recipes because missing one reduces user engagement and subscription revenue. The model must reach at least 80 percent recall for popular recipes.

This repository demonstrates an end-to-end data science workflow including:
Data validation, Data cleaning, Exploratory data analysis, Feature engineering, Baseline and comparison modelling, Threshold tuning for recall optimisation, Feature importance analysis, Business-focused insights

## Dataset
The dataset contains 947 recipes with the following attributes or features:
colaries, carbohydrate, sugar, protein, category, servings, high_traffic, recipe (identifier)

##Target Definition
The high_traffic column labels recipes that produced high traffic. Missing values were treated as Low traffic so that a complete binary target could be created. The target is defined as 1 for Popular and 0 for Unpopular.
This setup aligns with the business requirement for a binary classification problem.

## Objectives
- Predict whether a recipe will generate high traffic.
- Reach recall of at least 0.80 for the Popular class.
- Support the product team in selecting daily homepage recipes.

## Data Cleaning
I repaired the non-numeric values in the servings column, standardised inconsistent entries in the category column and imputed all missing nutritional data using median values. I removed the recipe identifier column because it does not contribute to the model, and I confirmed that the cleaned dataset contained no missing values before moving into the modelling stage.

## Exploratory Analysis
The exploratory analysis showed that popular recipes make up around 60 percent of the dataset, while unpopular recipes account for the remaining 40 percent. Chicken and vegetable dishes appear most frequently across the categories, whereas other groups such as pork and potato are less common. The analysis also indicated that unpopular recipes generally have lower nutritional values. The boxplots comparing calories, sugar, carbohydrate and protein revealed that popular recipes tend to have higher values in these nutritional metrics, showing a clear difference between the two groups.

EDA visuals:
Distribution plots for categories and target classes.
![Target Distribution Plot](images/DPURecipe)

Boxplots comparing nutritional features across recipe popularity.






