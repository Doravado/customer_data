# iFood Customer Data EDA

## Overview
- Created a new column as the unique identifier. Made a boxplot for each column and removed the outlier data. Visualized each column’s data distribution with histograms.

- Used cluster map, catplot, regplot to visualize the correlation between variables. Picked the optimal X variables to predict customer response, based on random forest results.

- Fitted the train data into three models (logit, probit, and c-log-log). Probit regression may be the best model for the data, with 87% accuracy after optimization.

- Plotted a histogram of response probability. The business can use the model to target customers who are more likely to respond and save more marketing costs.

![alt text](https://github.com/Doravado/ifood_customer_data/blob/main/image/confusion_matrix.png)
![alt text](https://github.com/Doravado/ifood_customer_data/blob/main/image/hist.png)

## Code and Resources Used
- Tools: Jupyter Notebook

- Packages: pandas, numpy, matplotlib, seaborn, statsmodel, sklearn

## Data Processing
- Created a column named 'Customer ID'. Summed up all types of purchases and added a new column 'TotalNumPurchases'.

- Created a boxplot for each column. According to the plots, the columns related to purchase amounts have a significant number of outliers.

- Calculated the mean and standard deviation of the columns with outliers and removed the data, which are three times standard deviations away from the mean.

![alt text](https://github.com/Doravado/ifood_customer_data/blob/main/image/boxplot.png)

## Data Distribution
- Created a histogram for each column. Except categorical data, most data have bell-shaped distribution.

![alt text](https://github.com/Doravado/ifood_customer_data/blob/main/image/datahisto.png)

## Data Correlation
- Used a cluster map to visualize the correlation between variables. The purchases of all kinds of products are highly correlated. Additionally, income and the number of kids are significantly correlated with many other variables.

- Based on catplot and regplot, age and purchase amount are positively correlated. Each age has a broad range of purchase amounts tough.

![alt text](https://github.com/Doravado/ifood_customer_data/blob/main/image/clustermap.png)

## Modeling Customer Response
- Used 'Response' as Y, and all other features as X. Based on the Random Forest outcomes, I picked 'Age', 'Complain', 'Customer_Days', 'Recency',  and 'MntTotal' as the X variables in the model.

- Fitted the train data into three models (logit, probit, and c-log-log), and compared their R-squared numbers. According to the results, probit regression may be the best model for the data, with 87% accuracy.

- Plotted a histogram of response probability. For the next campaign, the business can predict customer response probability based on their features and target customers more likely to respond. Targeting those customers rather than all customers can save more costs for the business.

![alt text](https://github.com/Doravado/ifood_customer_data/blob/main/image/important_feautres.png)
