<h1 align="center"> Airline Passenger Referral Prediction</h1>

<p align="center"> 
<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWlydzV2aHh0NG55ZHI2cHF4NzhjcHZ5NHhhdG01dmVhY2NhMDFhZyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/l1Kuh9tOmIQTt2L1C/giphy.webp" alt="..." height="500px">
</p>

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)



| **Sections**                                                                       |
|-------------------------------------------------------------------------------------|
| [Introduction](https://github.com/AIwithVivek/Airline_Passenger_Referral_Prediction#1-introduction) |
| [Exploratory Data Analysis (EDA)](https://github.com/AIwithVivek/Airline_Passenger_Referral_Prediction#2-exploratory-data-analysis-eda)   |
| [Key Insights from Visualizations](https://github.com/AIwithVivek/Airline_Passenger_Referral_Prediction#3-key-insights-from-visualizations) |
| [Data Pre-Processing](https://github.com/AIwithVivek/Airline_Passenger_Referral_Prediction#4-data-pre-processing) |
| [Models Used, Insights, and Metrics](https://github.com/AIwithVivek/Airline_Passenger_Referral_Prediction#5-models-used-insights-and-metrics) |
| [Model Selection and Considerations](https://github.com/AIwithVivek/Airline_Passenger_Referral_Prediction#6-model-selection-and-considerations)   |
| [Conclusions](https://github.com/AIwithVivek/Airline_Passenger_Referral_Prediction#7-conclusions)    |



![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)



# **Airline Recommendation Prediction**

## **1. Introduction**

The Airline Recommendation Prediction project aims to leverage machine learning techniques to predict whether a passenger would recommend an airline based on various attributes derived from their travel experiences. With the airline industry being highly competitive, the insights gained from this project can assist airlines in improving their services, understanding customer preferences, and making data-driven decisions.

### **Objectives:**
1. To classify airlines based on customer feedback and experiences.
2. To identify factors that influence customer recommendations.
3. To create a predictive model that can assist airlines in enhancing service quality.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


## **2. Exploratory Data Analysis (EDA)**

The EDA phase focused on understanding the dataset and uncovering patterns and trends. Key findings include:

1. **Cabin Class Preferences**: A bar chart visualization indicated that Economy class was the most preferred choice among travelers, with 45,171 passengers opting for it, followed by Business (9,590), Premium Economy (2,412), and First Class (1,532).
  
2. **Travel Trends Over Time**: An analysis of travel dates revealed peak travel months, with August 2015 being the busiest, followed by July 2018 and June 2018. This insight can help airlines prepare for high demand periods.
  
3. **Top Airlines by Popularity**: For the month of August 2015, the most favorable airlines identified were Spirit Airlines, American Airlines, United Airlines, British Airways, and Emirates Airlines, suggesting customer loyalty and satisfaction trends.
  
4. **Reasons for Travel**: A pie chart analysis indicated that Solo Leisure travel was the most common reason (37.1%), followed by Couple Leisure (25.8%) and Family Leisure (19%). This information is crucial for targeted marketing strategies.
  
5. **Customer Sentiment**: The overall recommendation level was found to be 47%, indicating a moderate customer sentiment, which implies significant opportunities for airlines to improve their services.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## **3. Key Insights from Visualizations**

Visualizations played a crucial role in understanding customer preferences and trends:

1. **Travel Route Preferences**: Analysis revealed that the route from Bangkok to London was the most frequently traveled, while routes from London to New York and Guangzhou to New York were less common.
2. **Rating Impact on Recommendations**: Higher ratings (above 8) were associated with recommendations, while ratings below 2 rarely resulted in recommendations. This highlights the importance of customer satisfaction in promoting loyalty.
3. **Feature Importance**: Correlation analyses indicated that the `value_for_money` and `overall` ratings were strongly correlated with customer recommendations, suggesting that improvements in these areas could enhance customer satisfaction.
4. **Trends Over Years**: The busiest year for air travel, as per the dataset, was 2018, with Spirit Airways, American Airlines, United Airlines, British Airways, and Emirates Airlines consistently being the top choices throughout the years.
5. **Service Ratings**: Consistent performance ratings across various categories, with 1-star ratings being most common for all service aspects, suggesting areas for potential improvement.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## **4. Data Preprocessing**

Data preprocessing is a critical step to ensure the quality and usability of the dataset. The following actions were performed:

1. **Handling Missing Values**: 
   - Numeric columns were imputed using the K-Nearest Neighbors (KNN) method, which considers the nearest neighbors to fill in missing data points.
   - The target variable (recommendation) was imputed using logistic regression, leveraging the relationship with other features.

2. **Encoding Categorical Variables**: 
   - Categorical features such as `traveller_type` and `cabin` were encoded using Label Encoding, transforming these textual data points into numerical format suitable for machine learning algorithms.

3. **Feature Scaling**: 
   - Numerical features were scaled to ensure that all input features contribute equally to model performance, enhancing the convergence speed of algorithms like KNN and ANN.

4. **Data Splitting**: 
   - The dataset was divided into training and testing sets, with an 80:20 split to ensure robust evaluation and prevent overfitting.

5. **Outlier Treatment**: 
   - Outliers were identified and treated to prevent skewed results and to ensure the models were trained on clean and representative data.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## **5. Models Used and Insights**

Several machine learning models were implemented to predict whether a customer would recommend an airline, including:

1. **Logistic Regression**: This model is beneficial for binary classification problems, such as predicting whether a customer would recommend an airline. It provides interpretable results, allowing stakeholders to understand the influence of various features.
  
2. **Random Forest Classifier**: A powerful ensemble method that operates by constructing multiple decision trees and merging their results. It is effective in handling overfitting and provides insights into feature importance.
  
3. **K-Nearest Neighbors (KNN)**: This model classifies instances based on the closest training examples in the feature space. It’s particularly useful for smaller datasets and can effectively capture local patterns.
  
4. **Support Vector Machines (SVM)**: This model is known for its effectiveness in high-dimensional spaces and is ideal for classification tasks where the boundary between classes is not linear.
  
5. **Artificial Neural Networks (ANN)**: A model that mimics the way human brains work. It is suitable for capturing complex relationships within the data, especially when there are many input features.

### **Insights from Model Evaluations:**
- **High Accuracy**: All models achieved impressive accuracy rates, with Logistic Regression showing an accuracy of 97% after hyperparameter tuning.
- **True Positive and True Negative Counts**: The ANN model had the highest true positive count (4,662), while the SVM model excelled in true negative classification (6,311).
- **Balanced Metrics**: Precision, recall, and F1 scores were consistently high across all models, indicating a well-rounded performance.

##To assess the performance of the models, several evaluation metrics were utilized:

1. **Accuracy**: The proportion of correct predictions made by the model.
2. **Precision**: The ratio of true positive predictions to the total predicted positives, indicating the model’s ability to avoid false positives.
3. **Recall**: The ratio of true positive predictions to the actual positives, reflecting the model's ability to capture all relevant cases.
4. **F1-Score**: The harmonic mean of precision and recall, providing a balance between the two metrics.
5. **ROC AUC Score**: The area under the Receiver Operating Characteristic curve, which evaluates the trade-off between true positive and false positive rates.


![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## **6. Model Selection and Considerations**

When selecting a model, it’s crucial to consider the context of the application:

1. **Understanding the Business Problem**: Different models might perform better depending on the consequences of false positives and negatives. For instance, if false negatives (not recommending a good service) are more critical, models with higher recall, like ANN, might be preferred.
  
2. **Model Complexity vs. Interpretability**: Simpler models like Logistic Regression are easier to interpret, while more complex models like ANN may provide better accuracy but are harder to explain to stakeholders.

3. **Computational Resources**: The choice of model may also depend on the available computational resources and the size of the dataset. For large datasets, Random Forest or SVM might be more suitable due to their robustness.

4. **Hyperparameter Tuning**: Techniques like Grid Search Cross Validation were employed to fine-tune the models, leading to improved performance metrics and better generalization on unseen data.

5. **Real-World Application**: It's essential to validate model performance using real-world data to ensure its applicability in practical scenarios. This can help in understanding the model's limitations and areas for further enhancement.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## **Conclusion**

In summary, the Airline Recommendation Prediction project has successfully demonstrated the application of machine learning techniques to analyze and predict customer behavior in the airline industry. The models employed, including Logistic Regression, Random Forest, K Nearest Neighbors, and Support Vector Machines, all exhibited high accuracy, indicating their effectiveness in predicting whether passengers would recommend an airline based on various features. 

Key insights reveal that customer satisfaction is heavily influenced by factors such as value for money, overall experience, and service quality. The project underscores the importance of understanding customer sentiment and preferences, enabling airlines to tailor their services accordingly. 

Moreover, the robust performance of the models suggests their readiness for deployment in real-world scenarios. Future work could explore feature importance and potential enhancements through advanced algorithms or ensemble methods, ensuring continual improvement and adaptability to changing customer needs. Overall, this project highlights the significant potential of data-driven approaches in enhancing service quality and customer satisfaction in the airline industry.



<p align="center"> 
<img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWdzZ21ib2N3OWJyYXZ1d3g5MnU3NjhqaWxxaXR3bXJ4dmF5bWV5OSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/P6q7wQz0wlcj6Nhzhd/giphy.webp"" alt="..." height="500px">
</p>
