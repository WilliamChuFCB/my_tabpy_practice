# Introduction to Tabpy

TabPy (the Tableau Python Server) is an Analytics Extension implementation which expands Tableau's capabilities by allowing users to execute Python scripts and saved functions via Tableau's table calculations.

This makes it possible to leverage Python’s machine-learning capabilities with the visualization power of Tableau, which can help us rapidly develop advanced analytics applications that can aid in various business tasks.

# About this project

This is a tiny tableau project that mainly uses two tabpy scripts respectively for PCA and machine learning classification, based on a breast cancer dataset that involves several numeric independent variables and a target variable suggesting whether the cancer type is malignant or benign. 

The final dashboard contains several parts:
- PCA Results: The datasource used in the tableau workbook includes 10 numeric variables. I used Principal Component Analysis (PCA) to reduce the dimension and utilized first two components to create a 2-D scatter plot, where the color of points indicates the cancer type.
- Exploration of PCA Variables: Although I used PCA to reduce 10 variables to 2, you can still figure out the relationship between original variables and these two principal components. When you choose an original variable in a dropdown menu, the color of the scatter points will gradient from large to small based on the selected variable value.
- Histogram: Since area, compactness and concavity represent three different and important dimensions of the cancer cells, I created histograms of these three varialbes respectively grouped by cancer type.
- Scatter Matrix: I also used area, compactness and concavity to produce a scatter matrix plot, which vividly display the relationship among these three variables and the data distributions of different cancer types.
- Prediction: In this part, user can enter the values to all the 10 variables regarding cancer cells. Then the calculated field will call the pre-trained SVM model established in a Python notebook and predict the cancer type. Finally, the dashboard also provides a small paragraph of diagnostic advice based on the predicted cancer type.
