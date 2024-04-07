# classification through the lens of occupancy detection
Utilizing a dataset that includes environmental parameters like Temperature, Humidity, Light, and CO2 levels within a room. The challenge here is to predict whether a room is occupied (Yes or No), turning raw data into actionable insights. This binary classification problem not only highlights the use of feature predictors in making precise classifications but also underscores the potential for such analysis in energy conservation, security, and smart building management.
The dataset can be found here: https://archive.ics.uci.edu/dataset/357/occupancy+detection

The dataset is pre-portioned into training and test sets, facilitating a straightforward approach to modeling. Our initial steps mirror those undertaken previously:
- Data Preprocessing and Cleaning: We ensure the dataset is free from inconsistencies and missing values, setting a solid foundation for analysis.
- Feature Engineering: By creatively manipulating the dataset, we enhance its utility for predictive modeling.
 
During our preliminary analysis, we observed that the 'Occupancy' variable is somewhat skewed towards the 'No' occupancy class. However, this skewness is not expected to significantly impact our model's performance.
A noteworthy observation is the high correlation between 'HumidityRatio' and 'Humidity', stemming from 'HumidityRatio' being a derivative of the latter two variables. Additionally, a strong correlation exists between 'Light' and 'Occupancy', suggesting that 'Light' could serve as a potent predictor for occupancy status.

## Analysis Results Summary
Our examination of various models for our binary classification problem reveals that Logistic Regression and Support Vector Machines (SVM) with a linear kernel stand out as particularly effective. These methods demonstrate superior performance by yielding metric values closest to 1, indicating a high level of accuracy.
This observation suggests that linear classifiers are more adept at handling this dataset, likely due to the binary nature of our dependent variable, which is categorized into two classes: 0 and 1. The effectiveness of linear classifiers in this scenario underscores their suitability for problems with a clear binary distinction between outcomes. Furthermore, to compensate for any potential skewness in the distribution of the output variable, we've adjusted the models by setting the class weights to 'balanced'. This parameter tweak ensures that our models are more equitable and accurately reflect the underlying data distribution.
