# Agriculture Production Web App

![pic1](assets/pic1.jpg)

## Click below to view the Web App
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://siddhantt-k-agriculture-production-app-x81l9j.streamlitapp.com/)

### Demo Images-

![HomePage](https://user-images.githubusercontent.com/87244972/180976973-fde76cc8-2591-4996-8455-f33dcd662a78.PNG)

![DataInfoPage](https://user-images.githubusercontent.com/87244972/180977660-6386f99d-f12e-4983-abce-3e95870f2fa3.PNG)

![VizPage](https://user-images.githubusercontent.com/87244972/180977690-b5a6d3a8-4610-4e7b-8fa3-60f19c44e88a.PNG)

![PredictPage](https://user-images.githubusercontent.com/87244972/180977708-3acf35e8-82a0-4a54-90e1-5482eba1c4e9.PNG)


## Key findings: Crops which require high ratio of both Phosphorous and Potassium in the soil are Grapes and Apple.


## Authors

- [@Siddhantt-K](https://www.github.com/Siddhantt-K)

## Table of Contents

  - [Business problem](#business-problem)
  - [Workflow](#workflow)
  - [Tech Stack](#tech-stack)
  - [Deployment on streamlit cloud](#deployment-on-streamlit-cloud)
  - [Repository structure](#repository-structure)


## Business problem

Since farmers need to deal with many problems amoung them few include how to :
        Cope with climate change
        Meet rising demand for more food of higher quality 
This web app suggests which crop/crops should be grown considering soil requirements and climatic conditions. This will help in decision making of farmers for the good quality and higher production of Crops. 


## Workflow

- Exploratory Data Analysis(EDA) : Descriptive Analytics.
                                   Used 'interact' function (from ipywidgets library) thoroughly for data analysis which creates a User Interface that has the control for exploring code and data interactively.
                                   For example, Checked summary stats (minimum, average, maximum) for each crop and have done few more analysis.

- Model Building : Performed 3 algorithms on the data- 1)K Means Clustering, 2)Logistic Regression and 3)Extreme Gradient Boost(XGBoost)
                   Used Unsupervised Machine Learning algorithm, K Means Clutering for cluster analysis to find which crops exhibits similar properties to be grown in the same soil requirement and climatic condition.
                   Applied Supervised Machine Learning algorithms ,Logistic Regression and XGBoost algorithms for the predictive modelling. 

- Serialization of Model : Saved the models using pickle.

- Evaluation of Model : Confusion Matrix, Classification Report.

- Production with Streamlit : Created a web app using Streamlit.


## Tech Stack

- Python (refer to requirement.txt file for the packages used in this project)
- Streamlit (interface for the model)


## Deployment on streamlit cloud

To deploy this project on streamlit share, follow these steps:

- First, make sure you upload your files on Github, including a requirements.txt file
- Go to [streamlit share](https://share.streamlit.io/)
- Login with Github, Google, etc.
- Click on new app button
- Select the Github repo name, branch, python file with the streamlit codes
- Click advanced settings, select python version 3.9 and add the secret keys if your model is stored on AWS or GCP bucket
- Then save and deploy!

## Repository structure

```

├── assets
│   ├── npk.jpg                                       <- Image used in web app
│   ├── icon.png                                      <- Streamlit web app icon image
│   ├── pic1.jpg                                      <- banner image used in the README
│   ├── HomePage.png                                  <- Home page (1st page) of the web app
│   ├── DataInfoPage.png                              <- Information page of the web app
│   ├── VizPage.png                                   <- Vizualization page of the web app
│   ├── PredictPage.png                               <- Prediction page (last page) of the multi page web app
│
├── datasets
│   ├── data                                          <- Dataset file.
│ 
├── Optimising Agriculture Production.ipynb           <- Main python notebook where all the analysis and modeling is done.
│
├── Agriculture_XGBoost_Model.pickle                  <- Pickle file of XGBoost classifier.
├
├── README.md                                         <- This is readme file.
│
├── app.py                                            <- File with the model and streamlit component for rendering the interface.
│
├── requirements.txt                                  <- list of all the dependencies with their versions.

```
