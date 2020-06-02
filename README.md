                                                  EDSA Sendy Logistics Challenge 
                                                    Machine Learning Predict

 Sendy Logistics Challenge Predict the estimated time of arrival (ETA) for motorbike deliveries in Nairobi
 ![download (3)](https://user-images.githubusercontent.com/60340826/83536563-acb87780-a4f3-11ea-9e9f-5271cf0666e1.jpg) 

 
                                                      Abstract
The purpose of this Predict project was to estimate time of delivery of orders from a point of driver pickup to the point of arrival at the final destination. For this regression model we have presented the training dataset with exploratory data analysis, test set, riders’ description and definitions of the variables. The Model was done by implementing data processing, feature engineering, feature selection, test split, machine learning and random forest. For the final model selected, Train RMSE of 561 and Test RMSE of 747 was obtained, our ranking score when submitting to zindi we got RMSE of 759.
                                                 
                                                 Introduction 
                                                 
In this regression model we had to participate in a Sendy logistic challenge which took place on Zindi. The solution will help Sendy enhance customer communication and improve the reliability of its service; which will ultimately improve customer experience. In addition, the solution will enable Sendy to realise cost savings, and ultimately reduce the cost of doing business, through improved resource management and planning for order scheduling.We were provided with datasets which are; train dataset that we used to train our model, test dataset on which we applied our model to, Riders which contains unique rider IDs, number of orders, age, rating and number of ratings, Variable Definitions which is the definitions of variables in the Train, Test and riders file. 
We prepared the comprehensive exploratory data analysis (EDA) using a training dataset. EDA includes the joining of different tables.The training dataset that was provided is a subset of over 20,000 orders and  only includes direct orders with bikes in Nairobi, all data in the subset given have been fully unidentified while preserving the distribution.we also had the data about the weather that corresponds to the time of the order.

Parameters/measures
Pandas
Jupyter notebook
Google colab
Sklearn
Joblib
                                           Data processing
                                           
 During  processing of data the train and riders dataframe were joined on the rider’s Id column, so as test and riders dataframe were also joined on rider’s Id column. We then drop the column from the test dataframe that is not present in raw data since the day of the month and weekday are duplicate and time cannot be reproduced. The list of columns that contain the same value from both raw_data and and test DataFrame was printed then the duplicate column in both DataFrame was dropped, we then investigated the Missing value.
                                  
                                        Feature Engineering
                                        
                                        
The AM and PM was extracted from pickup time and replaced pickup time with either AM or  PM, also extracted the AM and PM from arrival pickup time and replaced with either AM  or PM. The arrival at pick up time column was dropped , the number of a  day was replaced with the day name in pickup weekday then imputatiting was done. The redundant column was dropped to avoid the dummy variable trap.


                                       Feature selection 
                                       
 The running of the correlation, visualised the correlation with Heatmap. Performed the test split by splitting the data into X and Y, Train test split and scaling of data.
 
                                         Random forest
                                         
Experimenting with various cases of tree depth and max features at a node trying to find the optimum operating point and account for the bias vs variance trade off.

                                         Insights
                                         
Additional data doesn't add much to score;
Target encodings showed themselves pretty good;
Drivers characteristics (median speed, ratings, etc.) was quite good features;
Code refactoring from the jupyter notebook/google colab.
There are a few missing columns in the Test table.
The Train table seems to have columns that contain the same values.
The distribution of the data is narrow
Temperature and Precipitation in millimeters has a negative correlation






