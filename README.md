# Cryptocurrencies

A client has shown interest in offering a new cryptocurrencies investment portfolio for its customers. The data we will be working with is not ideal, so it will be processed to fit the machine learning models. Since there is no known output for what we are looking for, we decided to use unsupervised learning. 

1. Prepare the data for dimensions reduction with PCA and clustering using K-means.
2. Reduce data dimensions using PCA algorithms from sklearn.
3. Predict clusters using cryptocurrencies data using the K-means algorithm form sklearn.
4. Create some plots and data tables to present your results.

## Resources

  - Data Source: crypto_data.csv
  - Software: Python 3.7.6, Jupyter Lab 1.2.6
  - Libraries: Pandas, Plotly Express, Hvplot, Sklearn
  
## Summary

As you will see in the following steps below, we have ensured that all dependencies have been imported.

### 1. Data Processing

In this section, we load the information about cryptocurrencies and performed some data preprocessing tasks. Some of the taskes included the following:

   - Remove all cryptocurrencies that aren't trading, that don't have an algorithm defined, with a least one null value, and without coins mined.
   - Create a new DataFrame named coins_name that stores the names of all cryptocurrencies and set the index with the column named *'Unnamed: 0'*.
   - Create dummies variables for all the text features and store the resulting data in a DataFrame named X.
   - Standardize all the data with *StandardScaler*.
   
### 2. Reducing Data Dimensions Using PCA
 
   - We used the *PCA algorithm* from sklearn to reduce the dimensions of X down to 3 principal components.
   
By doing this, we can see how much weight the columns have for each component.
   
### 3. Clustering Cryptocurrencies Using K-means

Unlike with supervised learning, we do not have a value for K. In order to find that value, we need to complete the following tasks:

  - Create an elbow curve to find the best value for K. As you will see in the code, the best value is 4.
  - Run the K-means algorithm to predict the K clusters for the cryptocurencies' data.
  - Create a new DataFrame named *'clustered_df'* to visualize our results.
  
### 4. Visualizing Results

There will be a time when the best way to present your results is through the use of visualizations. Not everyone you present your results will understand data preprocessing, scaling or K-means. We presented the data in the following ways:

  - Create a 3D scatter plot using Plotly Express. When you run the code, you will be able to interact with the data points.
  - Use *hvplot.table* to create a data table with all the current tradable cryptocurrencies.
  - Create a scatter plot using *hvplot.scatter* to present the clustered data about cryptocurrencies having x='TotalCoinsMined' and y='TotalCoinSupply' to contrast the number of available coins versus the total number of mined coins. This plot is considered as a 2D version of the 3D plot.
  
## Usage
**Note:** Please ensure you have all the required and updated softwares on your computer.

  1. Download the following files into the same folder for the project.
      
      - crypto_data.csv
      - Cryptocurrency_Analysis.ipynb

  2. In your Anaconda prompt, activate your development environment and navigate to the folder holding the above files and run Jupyter Notebook. For this specific project, Jupyter Notebook will render the plots. If you want to run the visualizations in Jupyter Lab, you will need to install a few things first. You can check out what is needed at https://plotly.com/python/getting-started/#jupyterlab-support-python-35.

  3. You can now run all the cells to see their outputs. If you want to test out the results, you can change the parameters.
 

