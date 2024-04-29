# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE
Emily Essam Kamel
## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: Add your explanation
I realized that the changes made in the last two submissions improved the square error
I needed to change or add some features in order to make the model learn more accuratelly and also changing some hyperparameters could decrease the error
### What was the top ranked model that performed?
TODO: Add your explanation
the last submission :submission_new_hpo
my explanation for this: the last submssion has more features to train on so it could understand the relations between the features more acurrately and the finetuning step also 
## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: Add your explanation
creating histograms could help in visulaizing how the data is distributed and what are numerical features and what are categorical
I added some new features by separating the datetime column into three new features (day,month,hour) which helped the model into understanding more what datetime means and what is its relation to other features
### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation
improved by 34%
adding new features (feature engineering) could help the model to understand the relations between the features in a more accurate way
## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation
improved by 91%
num_trials:This hyperparameter specifies the number of trials or iterations to perform during hyperparameter tuning. The purpose of hyperparameter tuning is to find the best combination of hyperparameters that results in the optimal performance of the model.
searcher: This hyperparameter specifies the search strategy to use during hyperparameter tuning. The search strategy determines how the different combinations of hyperparameters are explored and evaluated.
all these hyperparamter could improve the model and add some more complexity to it 
### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation
on feature engineering and on exploring different hyperparamters
### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|?|?|?|?|
|add_features|?|?|?|?|
|hpo|?|?|?|?|

"model": ["initial", "add_features", "hpo"],
    "hpo1": ["time_limits", "presets","train"],
    "hpo2": ["time_limits", "presets","train_new_features"],
    "hpo3": ["num_trials", "searcher", "scheduler"],
    "score": [1.80992, 0.61877, 0.56652]
}
### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](nd009t-c1-intro-to-ml-project-starter/model_train_score.png)


### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](nd009t-c1-intro-to-ml-project-starter/model_test_score.png)


## Summary
TODO: Add your explanation
in the training : adding new features had the best score evaluation
in the test: adding new hyperparameters with new features had the best score evaluation
Sometimes, adding new features during training can help the model learn more complex patterns and improve its performance. However, adding new hyperparameters during testing can fine-tune the model's behavior and optimize its performance on unseen data.