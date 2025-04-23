## Cancer detector
The goal of the project is to build a classification model that accurately predicts outcomes based on available features. The project involves applying various preprocessing techniques, such as standardization and PCA, and comparing the results of different classification models like KNN, logistic regression, and boosting. The ultimate aim is to achieve the highest model accuracy and select the most effective classification method based on the experiments conducted.

In this step, the dataset was loaded using the pandas library and its structure was previewed with the head() function. This allowed for a quick inspection of the first few rows to understand the available features and data format.
![image](https://github.com/user-attachments/assets/7ed01a70-ca05-4086-8d0a-4052aeeff687)

In this step, basic statistical analysis was performed using the describe() function to summarize the dataset. It provided insights into the distribution, central tendency, and spread of each numerical feature.
![image](https://github.com/user-attachments/assets/2e81995c-8c47-4746-a610-6213920237f3)

In this step, a heatmap of the correlation matrix was generated to visualize the relationships between selected features. This helped identify which features are strongly correlated and may impact model performance or feature selection.

![image](https://github.com/user-attachments/assets/eb6047f0-e68e-4fe6-902f-643c72a65a4c)

In this stage of the project, I didn't apply any preprocessing steps like standardization or PCA. I assigned the feature matrix X to the entire dataset df, and the target variable y to the 'diagnosis' column.

![image](https://github.com/user-attachments/assets/71394be2-31c5-478c-9fc2-d9b6a6db8910)

In this step of the project, I applied standardization to the dataset using the StandardScaler. I transformed the entire dataset df and created a new DataFrame std_df with the standardized values, and then assigned the feature matrix X and target variable y as before.

![image](https://github.com/user-attachments/assets/8ac04b56-7341-41bf-973b-13f8f6ac7822)

In this step, I applied both standardization and Principal Component Analysis (PCA). First, I standardized the dataset using StandardScaler, then performed PCA with 95% explained variance, reducing the dataset's dimensionality. The transformed dataset was assigned to pca_df, and I also printed the explained variance ratio for each principal component. Finally, I assigned the transformed features to X and the target variable y as before.

![image](https://github.com/user-attachments/assets/4bc21b76-aa4d-4a79-95cf-0eb848cb29c2)

In this part of the project, I used the train_test_split function to divide the data into training and test sets. The training data size is 398, while the test data size is 171, and the split was made with 30% of the data reserved for testing.

![image](https://github.com/user-attachments/assets/1570bd73-ca80-4400-a879-7373dc737f04)

In this part of the project, I plotted the relationship between the number of neighbors and model performance, showing how the model accuracy varies with different values of neighbors. The plot indicates that the highest model accuracy (97.08%) was achieved with 9 neighbors, improving the model accuracy by 2.92%.

![image](https://github.com/user-attachments/assets/ee7a1c2b-71d8-4b68-9fd5-04230e47c082)

In this part of the project, I compared the results of different models by plotting their performance. The bar chart shows the accuracy of various models, with the highest performing model being Logistic Regression, followed closely by other classifiers such as KNeighborsClassifier, AdaBoostClassifier, and GradientBoostingClassifier.

![image](https://github.com/user-attachments/assets/1f3f533e-e59f-460d-9c6c-7a564f8c36f5)


### Conclusions from the project:
In the project, data analysis was performed using various preprocessing techniques such as standardization and PCA, and the performance of different classification models was compared. Initially, the data was prepared without any preprocessing, then standardization was applied, followed by PCA to reduce the dimensionality while retaining 95% of the variance. The models were split into training and test sets, and experiments with different numbers of neighbors in the KNN algorithm were conducted, leading to the best result. The model comparison results indicate the highest accuracy achieved by the logistic regression model, suggesting its better fit to the data compared to other algorithms. The takeaway from the project is that logistic regression, along with proper data preprocessing (standardization and PCA), results in high model accuracy.
