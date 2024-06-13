# Cryptocurrency Clustering Analysis


## Overview
This project uses Python and unsupervised learning techniques to predict whether cryptocurrencies are affected by 24-hour or 7-day price changes. The analysis involves clustering the cryptocurrencies using K-Means, both with the original data and after optimizing with Principal Component Analysis (PCA).

## Requirements
Find the Best Value for k Using the Original Data
To find the best value for 𝑘, the elbow method algorithm was coded using a range from 1 to 11. This involved plotting a line chart of all the inertia values computed with the different values of 
𝑘 to visually identify the optimal value. The best value for 𝑘 was determined to be 4.

### Cluster the Cryptocurrencies with K-Means Using the Original Data
After identifying the best value for 𝑘, the K-Means model was initialized with four clusters. The model was then fit using the original data, and the clusters for grouping the cryptocurrencies were predicted. The resulting array of cluster values was reviewed, and a copy of the original data was created with a new column for the predicted clusters. Using hvPlot, a scatter plot was created with x="price_change_percentage_24h" and y="price_change_percentage_7d". The points were colored with the cluster labels, and the cryptocurrency names were added to the hover columns to identify each data point.

### Optimize the Clusters with Principal Component Analysis
A PCA model instance was created and set with n_components=3 to reduce the features to three principal components. After transforming the data, the first five rows of the resulting DataFrame were reviewed. The explained variance was determined to understand how much information each principal component captured, and the total explained variance was calculated. A new DataFrame was created with the PCA data, setting the coin_id index from the original DataFrame as the index for the new DataFrame, and the resulting DataFrame was reviewed.

### Find the Best Value for k Using the PCA Data
The elbow method algorithm was applied to the PCA data to find the best value for 𝑘, using a range from 1 to 11. A line chart of the inertia values computed with different values of 
𝑘 was plotted to visually identify the optimal value. The best value for 𝑘 when using the PCA data was determined and compared with the best value found using the original data.

### Cluster the Cryptocurrencies with K-Means Using the PCA Data
The K-Means model was initialized with the optimal number of clusters found using the PCA data. The model was then fit using the PCA data, and the clusters for grouping the cryptocurrencies were predicted. The resulting array of cluster values was reviewed, and a copy of the DataFrame with the PCA data was created with a new column for the predicted clusters. Using hvPlot, a scatter plot was created with x="PCA1" and y="PCA2". The points were colored with the cluster labels, and the cryptocurrency names were added to the hover columns to identify each data point.

### Visualize and Compare the Results
A composite plot was created using hvPlot to compare the elbow curve from the original data with the one from the PCA data. Additionally, another composite plot was created to compare the cryptocurrency clusters resulting from the original data with those from the PCA data. Based on this visual analysis, the impact of using fewer features to cluster the data with K-Means was discussed.

## Coding Conventions and Formatting
To maintain code readability and quality:

Imports were placed at the top of the file, just after any module comments and docstrings, and before module globals and constants.
Functions and variables were named with lowercase characters, with words separated by underscores.
DRY (Don't Repeat Yourself) principles were followed to create maintainable and reusable code.
Concise logic and creative engineering were used where possible.

By following these guidelines, the project demonstrates the ability to use unsupervised learning techniques to analyze and cluster cryptocurrency data, providing valuable insights into the effects of 24-hour and 7-day price changes.

## Credits
Tiffany La Mar

## Contact
If there are any questions of concerns, I can be reached at:
##### [github: teelam1910](https://github.com/teelam1910)
##### [email: tiffanylamarj@gmail.com](mailto:tiffanylamarj@gmail.com)

## Resources
- ASU/EdX Tutoring
- Class Activities
- https://cloud.google.com/discover/what-is-unsupervised-learning#:~:text=Unsupervised%20learning%20in%20artificial%20intelligence,any%20explicit%20guidance%20or%20instruction.
- https://www.geeksforgeeks.org/ml-types-learning-part-2/
- https://www.youtube.com/@thinking_neuron
- https://www.youtube.com/watch?v=Vi1CwSU4IyU
- https://www.youtube.com/watch?v=D6gtZrsYi6c
- https://www.youtube.com/watch?v=gZ0e40wgdDc&list=PLOLWGEXpOrByXHRGMfU1b7X4esb-c1i2N
- https://hvplot.holoviz.org/user_guide/Plotting.html
- https://hvplot.holoviz.org/reference/tabular/line.html
- OpenAI
