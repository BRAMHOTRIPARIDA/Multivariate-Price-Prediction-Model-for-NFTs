Multivariate Price Prediction Model for NFTs 
----------------------------------------------- 
Objective of Project : Develop sales data driven NFT price forecasting model using Deep Learning model architectures for sequential data analysis.  

Estimated NFT Collections prices by harnessing market indicators such as Google Trends with a validation error range 0.05-10 RMSE for different Collections.
The system contains deep learning recurrent neural network model to generate NFT market price predictions using GRU-RNN based time series forecasting models.
The prices of NFTs are forecasted for next 5 days on a sliding basis to help make informed decisions and also analyze the market trends.


Dataset : 
1) NFT Market data - OpenSeas API
2) Relative Search Volumes of Collections - Google Events

The dataset is divided into categories - Arts/Games/Collectibles

![image](https://user-images.githubusercontent.com/26669836/207478432-ad299f80-55c1-4ff6-b4e3-0ed9d4822583.png)


Methodology - Features and Model
-----------------------------------------------
![image](https://user-images.githubusercontent.com/26669836/207477736-37e6773e-f2da-4063-bb23-8541a6295240.png)

The GRU-RNN models have been built for individual Collections to understand and analyze the model performance. Since tokens within a Collection have a similar signature style and trend, prices are aggregated for Collections which is representative of the individual NFT tokens. The RMSE scores have been estimated and vary differently based on the scale of prices of different Collections.

Number of NFT transactions per day has been used as a threshold feature to remove data points which are more likely to be outliers in the dataset.

Google trends relative search volumes of Collections have been added as features to the model and affect the prices of Collections.

Sliding windows are used to predict the price of NFTs for the next 5 days dynamically by fetching data from the APIs listed above.

The multivariate data has been preprocessed and transformed using Standard Scaler and then training and validation sets are created which is used for training the Deep Learning models by fine tuning the hyper parameters of the models.
