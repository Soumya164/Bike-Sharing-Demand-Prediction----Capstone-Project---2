# Bike-Sharing-Demand-Prediction----Capstone-Project---2

Google colab Access link :- https://colab.research.google.com/drive/12DcMIuPVJG-hH_Fd0-UqpLGYZn3F0AIZ#scrollTo=RAe8T6hvus9h

CONCLUSION
During the time of our analysis, we initially did EDA on all the features of our datset. We first analysed our dependent variable, 'Rented Bike Count' and also transformed it. Next we analysed categorical variable and dropped the variable who had majority of one class, we also analysed numerical variable, found out the correlation, distribution and their relationship with the dependent variable. We also removed some numerical features who had mostly 0 values and hot encoded the categorical variables.

Next we implemented 7 machine learning algorithms Linear Regression,lasso,ridge,elasticnet,decission tree, Random Forest and XGBoost. We did hyperparameter tuning to improve our model performance. The results of our evaluation are:

# displaying the results of evaluation metric values for all models
result=pd.concat([training_df,test_df],keys=['Training set','Test set'])
result
Model	MAE	MSE	RMSE	R2_score	Adjusted R2
Training set	0	Linear regression	4.444	34.810	5.900	0.774	0.77
1	Lasso regression	7.242	91.458	9.563	0.406	0.39
2	Ridge regression	4.444	34.810	5.900	0.774	0.77
3	Elastic net regression	5.765	57.415	7.577	0.627	0.62
4	Dicision tree regression	5.196	49.927	7.066	0.676	0.67
5	Random forest regression	0.812	1.630	1.277	0.989	0.99
6	Gradient boosting regression	3.254	18.594	4.312	0.879	0.88
7	Gradient Boosting gridsearchcv	1.848	7.398	2.720	0.952	0.95
Test set	0	Linear regression	4.373	33.085	5.752	0.791	0.79
1	Lasso regression	7.442	96.685	9.833	0.388	0.37
2	Ridge regression	4.373	33.087	5.752	0.791	0.79
3	Elastic net regression Test	5.846	59.380	7.706	0.624	0.62
4	Dicision tree regression	5.390	56.318	7.505	0.643	0.64
5	Random forest regression	2.231	12.881	3.589	0.918	0.92
6	Gradient boosting regression	3.477	21.311	4.616	0.865	0.86
7	Gradient Boosting gridsearchcv	2.367	12.059	3.473	0.924	0.92
• No overfitting is seen.

• Random forest Regressor and Gradient Boosting gridsearchcv gives the highest R2 score of 99% and 95% recpectively for Train Set and 92% for Test set.

• Feature Importance value for Random Forest and Gradient Boost are different.

• We can deploy this model.

However, this is not the ultimate end. As this data is time dependent, the values for variables like temperature, windspeed, solar radiation etc., will not always be consistent. Therefore, there will be scenarios where the model might not perform well. As Machine learning is an exponentially evolving field, we will have to be prepared for all contingencies and also keep checking our model from time to time. Therefore, having a quality knowledge and keeping pace with the ever evolving ML field would surely help one to stay a step ahead in future
