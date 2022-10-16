# Neural_Network_Charity_Analysis
# Overview of the analysis: 
Alphabet Soup is a non-profit organization dedicated to protecting the environment. The Company invests in life-saving technology and the organization of reforestation groups around the world. Alphabet Soup invests in many partner companies that carry out the strategic goal of saving the environment.
In the project, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Using knowledge of machine learning and neural networks, we will use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
 
## Control Flow
1- Data Preprocessing
2- Feature and Target Selection
3- Splitting the dataset to train and test
4- Fitting and predicting with he model
5- Evaluating model performance
6- Evaluate Feature importance (Depending on model)
6- Optimize model based on Feature Importance or other model parameters or features

## Results
Data Preprocessing
Feature and Target Selection
- The variable considered the target for our model is "IS_SUCCESSFUL"
- The variables considered to be the features for our model are :

		- EIN
		- NAME
		- APPLICATION_TYPE
		- AFFILIATION
		- CLASSIFICATION
		- USE_CASE
		- ORGANIZATION
		- STATUS
		- INCOME_AMT
		- SPECIAL_CONSIDERATIONS
		- ASK_AMT

- The variables that we dropped from the input data are "EIN" and "NAME".
Compiling, Training, and Evaluating the Model
To optimize the model, 
Attempt 1: we used three hidden layers, with 85, 35, and 10 neurons for layer1, layer2, and layer3 respectively. 

![1st_attempt_85_35_10](https://user-images.githubusercontent.com/103543959/196058666-004aa999-9113-4b93-9b96-7fc377019975.png)

Attempt 2: we used three hidden layers, with 90, 70, and 50 neurons for layer1, layer2, and layer3 respectively

![2st_attempt_90_70_50](https://user-images.githubusercontent.com/103543959/196058673-0421275f-0d35-4c3b-acc9-a9cf0610335e.png)

Attempt 3: we used three hidden layers, with 100, 50, and 20 neurons for layer1, layer2, and layer3 respectively

![3rd_attempt_100_50_20](https://user-images.githubusercontent.com/103543959/196058678-5e85df22-4049-47b7-9542-9bf04b99a445.png)

Attempt 4: We tried the ramdom Forest model instead with three hidden layers, with 100, 70, and 300 neurons for layer1, layer2, and layer3 respectively.Then we also changed the activation type the sigmoid for the input and rely for the output.That decreased our model performance

![4th_attempt](https://user-images.githubusercontent.com/103543959/196058688-a6399dc1-c30d-41d8-a8f9-50dbad469ef4.png)

Attempt 5: we used three hidden layers, with 30 and 20 neurons for layer1, layer2, and  removed layer3.

![73%](https://user-images.githubusercontent.com/103543959/196058721-9651d43d-c4d3-4d41-84fe-2327fadad7ec.png)

![735](https://user-images.githubusercontent.com/103543959/196058704-ed144e0d-6756-4092-97d1-957fcfdcb83a.png)


Summary
While the neural network model may be a robust machine learning algorithm, it did not do an excellent job at classifying which applicant's requests for donation will be successful given the dataset we have. Some of the steps to improve model accuracy may include:

One recommendation is to use a larger dataset to train the neural network model to learn the general distribution of the dataset without overfitting.
We may use the Balanced Random Forest Classifier, which combines the decision of multiple trees to create a strong model accuracy
While model accuracy reached 73%, we may have a model that is overfitting. That is why a larger dataset will be appropriate to train our neural network model or any other model we choose to use.
