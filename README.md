Titanic Survival Data Analysis
==============================

This is my initial analysis of the Titanic survival dataset from the Kaggle competition. The dataset contains a train.csv and test.csv from the Kaggle competition website. The analysis involves data cleaning and machine learning analysis with logistic regression, decision tree, random forest and a couple of other machine learning tools to make predictions. Predictions are saved in 'processed' data as 'submissions.csv'

Goals for this project
------------

To show an example of analysis in Python (Python 3) on the Titanic dataset. 
Jupyter notebooks (located in notebooks) were used for initial data exploration, model comparisions, and visualizations. Final, cleaned versions of the code to make the final dataset, perform the analysis, and make visualizations were saved as .py formats.

The data saved in '/data/processed' and the output figures can be generated by first navigating to the 'titanic_Kaggle' directory, then executing the python code in the following order:

   1. run >python /src/features/bulid_features.py
   2. run >python /src/models/predict_model.py
   3. run >python /src/visualization/visualize.py

Project Organization
------------

    ├── LICENSE
    ├── README.md          <- The top-level README
    ├── data
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── models             <- model summaries
    │
    ├── notebooks          <- Jupyter notebooks
    │
    ├── reports            
    │   └── figures        <- Generated graphics and figures 
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py


--------

#####

VARIABLES | DESCRIPTION
----------|------------
Survival | (0 = No; 1 = Yes)
Pclass   |  Passenger Class (1 = 1st; 2 = 2nd; 3 = 3rd)
Name     | Name
Sex      |  Male or Female
Age       |  Age in years
Sibsp     |  Number of Siblings/Spouses Aboard
Parch     |  Number of Parents/Children Aboard
Ticket    |  Ticket Number
Fare      |  Passenger Fare
Cabin     |  Cabin
Embarked  |  Port of Embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)

#####

SPECIAL NOTES:

Pclass is a proxy for socio-economic status (SES) (1st ~ Upper; 2nd ~ Middle; 3rd ~ Lower)

 
Age is in Years; Fractional if Age less than One (1)
   If the Age is Estimated, it is in the form xx.5
   
   
With respect to the family relation variables (i.e. sibsp and parch)
some relations were ignored.  The following are the definitions used
for sibsp and parch:


Sibling: Brother, Sister, Stepbrother, or Stepsister of Passenger Aboard Titanic


Spouse:  Husband or Wife of Passenger Aboard Titanic (Mistresses and Fiances Ignored)


Parent:  Mother or Father of Passenger Aboard Titanic


Child:   Son, Daughter, Stepson, or Stepdaughter of Passenger Aboard Titanic

Other family relatives excluded from this study include cousins,
nephews/nieces, aunts/uncles, and in-laws.  Some children travelled
only with a nanny, therefore parch=0 for them.  As well, some
travelled with very close friends or neighbors in a village, however,
the definitions do not support such relations.

Acknowledgments
------------

* Cookiecutter-data-science template was used for file orgainization (<a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>)

* Competition Website: <a target="_blank" href="http://www.kaggle.com/c/titanic-gettingStarted">Titanic: Machine Learning from Disaster</a>


