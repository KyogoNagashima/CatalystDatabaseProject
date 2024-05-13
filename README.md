# CatalystDatabaseProject

## Project Description
It is not an understatement to say that the modern-day lifestyle is supported by various chemical commodity products. However, the chemical industry heavily relies on the use of extremely harsh conditions to surpass the thermodynamic and kinetic barrier associated with reacting small abundant molecules. To enable these harsh conditions, a lot of energy must be inputted, releasing large amounts of carbon-dioxide and other greenhouse gases into the atmosphere. However, by inserting chemicals known as catalysts into the reaction, we can enable easy production of these high-value commodity products without the use of harsh conditions. A criterion for assessing the efficiency of these catalysts is its adsorption energy. The adsorption energy tells us how favorable it is for a certain small molecule to attach onto the catalyst surface. In this study, we utilize the Catalyst Database compiled by the ChemCatBio initiative which is a database that consists of adsorption energies of various catalysts and small molecule adsorbents. We employed various machine learning algorithms such as support vector machines, decision trees, random forests, and neural networks to predict adsorption energies using this data. It was found that random forests performed the best out of all the models revealing important attributes for predicting adsorption energies, providing additional insight into how chemical catalysts work. 

## How to Use/Look at the Project
The project is composed of multiple jupyter notebook files. 

### 1. Load Dataset
This notebook loads the JSON file that contains the catalyst properties and extracts only the relevant portions. Since the dataset is in JSON format, it was reformatted into a pandas dataframe and also save as a csv file. Running the jupyter notebook will automatically generate a csv file. 

### 2. Clean Dataset
Because the dataset contains many irrelavant attributes and missing data, this jupyter notebook goes through each of them and cleans the dataset. Many attributes were omitted from the dataset and missing values were filled up using imputation. Finally, a full dataset with all possibly relevant attributes was made. 

### 3. Create Dataset
Using the full dataset created in the previous notebook, the data was further divided into dataset 1) which only contain information on the adsrobent, dataset 2) which contains information on both the adsorbent and catalyst, and dataset 3) which contain information on the adsorbent, catalyst, and the method. Upon analysis of the data using neural networks, dataset 2 predicted the adsorption energies the best and therefore dataset 2 was used for further analysis. 

### 4. Analyze Dataset 2
Here, various machine learning models were applied to dataset 2. Specifically, traditional neural networks, linear regression, ridge regression, LASSO regression, decision trees, random forests, and SVM of various kernels were tested. 

