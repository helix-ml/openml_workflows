# OpenML Scikit-Learn Workflows

The data for 475,297 machine learning runs provided in the .csv file were directly derived from https://www.openml.org/.

In relation to our HILDA paper, a **run** corresponds to a single row in the .csv file, and a **sequence** is a groupby on user\_id and task\_id. 

The columns in the .csv are as follows:
- **rid**: Run id on OpenML
- **user\_id**: User id on OpenML
- **task\_id**: Task id on OpenML
- **auc**: Area under ROC curve of the run
- **dist\_from\_mean\_auc**: Relative performance--difference between the AUC of the run and the mean AUC of all the runs for the same task\_id
- **model**: Set of Scikit-Learn classifiers/estimators and model wrappers used in the run
- **model\_params**: Set of model hyperparameters represented as (parameter name, parameter value) tuples
- **ppr**: Set of preprocessing operators (note that "set()" means that no preprocessing was used)
- **ppr\_params**: Set of preprocessing hyperparameters represented as (parameter name, parameter value) tuples
- **iter**: Iteration of the run in the sequence (starting from 1)
- **change\_type**: Type of change from the previous iteration:
  - 'S': Starting iteration
  - 'M': Model operator change
  - 'P': Preprocessing operator change
  - 'H': Model Hyperparameter change
  - 'R': Preprocessing hyperparameter change
  - 'C': Combination of model and preprocessing changes (operator or hyperparameter)
  - 'N': No change
- **delta\_auc**: Change in AUC from the previous iteration
- **start\_time**: Start time of the run
- **time\_delta\_in\_mins**: Difference between the start time of the current iteration with the previous iteration
