# Traffic-Data-Analysis-and-count-prediction-NY
Real world Dataset of County  wise Traffic counts (of size: >50000 entries) is analyzed and traffic counts were predicted using ML algorithms and later this dataset was combined with New York County wise Population dataset to visualize the correlation and its affect to the traffic counts. 

As Datasets for this project are beyond GitHub repository limit. Below are the links to access the datasets from the official sites:

Annual Average Daily Traffic Dataset link: https://data.ny.gov/Transportation/Annual-Average-Daily-Traffic-AADT-Beginning-1977/6amx-2pbv
Annual Population Estimates for New York State and Counties: https://data.ny.gov/Government-Finance/Annual-Population-Estimates-for-New-York-State-and/krt9-ym2k/data The above information can also be found in link_for_datasets document.
Regarding Datasets:

Annual Average Daily Traffic (AADT) is an estimate of the average daily traffic along a defined segment of roadway. This value is calculated from short term counts taken along the same section which are then factored to produce the estimate of AADT. Because of this process, the most recent AADT for any given roadway will always be for the previous year. Data is available for all New York State Routes and roads that are part of the Federal Aid System.

Annual Population Estimates for New York State and Counties: Resident population of New York State and counties. Estimates are based on Census counts (base population), intercensal estimates, and postcensal estimates.

In this project, working on real world data like traffic was very challenging. As we know real world data will not be clean. Annual Average Daily Traffic Dataset considered has around 60k+ entries/samples. Data has been pre-processed, analyzed and visualize initially. As part of pre-processing of the data, samples which belong to years other than 2019 were excluded as the original dataset has more than 2.5 Million samples. And from the selected Traffic data of year 2019, there was a lot of missing data present which needs to be handled. Data imputation techniques where used to handle missing data. For few variables, more than 85% of data was missing but as the variable type is similar to boolean and later it was found from the table metadata that the values missing represent 'No' (for most of them). For these columns missing values were replaced with a 'N'(with 'local' for Signing column). Later encoding has been done for the categorical data for further predictions. Interesting patterns like correlation between different variables were visualized from the data.

From the above visualization, we can identify the columns which affect the counts column (as it is the response column). And as part of data cleaning for prediction and analysis, few columns which did not affect the response variable 'count' have been eliminated. The other missing values where filled with the help of random value imputations and for few regression techniques (like linear regression and KNN) were used.

Machine Learning Algorithms like Linear Regression', 'SVR', 'Decision Tree Regressor','Elastic-Net', 'SGD Regressor', 'MLP Regressor', 'Random Forest Classifier were used to model the target variable. It was observed that Decision Tree Regressor works very efficiently in predicting the traffic counts for the test data compared to remaining models. And the performance of the Decision Tree model was expected as the data was hybrid type where categorical variables were dominating the target variable.

Annual Population Estimates for New York State Dataset has been combined with the existing Traffic data and statistical analysis was perfomed on the selected features to find the correlation. And in the end of this analysis interesting patterns were found, analysed and visualized.
