# CryptoClustering
UTSA Data Analytics Bootcamp Unsupervised Machine Learning challenge to determine if cryptocurrency value is affected by 24-hour or 7-day price changes and how PCA will affect our analysis.

------------------------------------------------------------------------------------------------------------------
crypto_clustering.ipynb

Within the CryptoClustering repository there is the crypto_clustering.ipynb jupyter notebook file that contains the Python code for running clustering analysis using unsupervised machine learning on cryptocurrency data.

Cryptocurrency data is extracted from the crypto_market_data.csv in the Resources folder and is then added to a pandas DataFrame. 

The data is then prepared using standard scaling and the data is indexed by cryptocurrency ID. The analysis of the data is then taken in two different directions. First, original scaled data is fit to a KMeans model and inertia values for each value of k within a range of 1-11 is plotted on an elbow curve to visually determine the best value for k. 

The Kmeans model is then used to predict and create clusters for the cryptocurrency data. The resulting clusters are then added to the DataFrame and plotted on a scatterplot for each cryptocurrency.

Secondly, the clustering is then optimized using principal component analysis to reduce number of contributing features to clustering. A PCA model is created with three features and total variance is assessed at 85%. The previous steps are then repeated where an elbow curve is used to determine the most appropriate value of k, and the KMeans model is then applied and clusters are once again plotted.

Resulting elbow curves and clustering are then compared between models using original data and optimized PCA data.