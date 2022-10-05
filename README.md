# CI/CD pipeline using Flask machine learning app

# Overview of the project
Sklearn model has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. This project operationalizes a Python flask app—in a provided file, app.py that serves out predictions (inference) about housing prices through API calls. I have used Azure pipelines for continuous deployment.
# Architectural Diagram
![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/architecture.JPG)
# Instructions for running the Python project
![Python application test with Github Actions](https://github.com/manas1230/flask_devops/actions/workflows/pythonapp.yml/badge.svg?branch=scaffolding)

I have set up continuous integration using github to test the make/requirements files. The make test pass wihtout any error (also confirmed with YAML file in github actions)
![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/make%20test%20pass.JPG)

Below is a screenshot of cloning the git repo in azure cloud shell before moving on to the main flask project.
![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/git%20clone%20repo%20cli.JPG)

![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/pythonapp%20yml%20pass.JPG)

Next, An azure webapp service is launched to host the flask machine learning app as shown below.
![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/webapp.JPG)

After the web app launched successfully, 
![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/webapp%20launch1.JPG)

A Linux virtual machine was created to be the agent to handle the deployment in Azure devops.
![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/deploy%20pipelines.JPG)

The Azure pipelines uses a self hosted feature by making use of the git repo to automatically build the YAML file. This YAML file/script builds and deploys the app into our webapp.

This is a successfull prediction after deploying the flask app
![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/prediction.jpg)

I have also run locust load tests with 10 users
![alt text](https://github.com/manas1230/flask_devops/blob/main/screenshot/locust.JPG)

# Project plan followed
The Project deliverables is tracked using the below tools-

https://trello.com/b/L3d1vTMr/flask-project-plan

https://github.com/manas1230/flask_devops/blob/main/screenshot/project-management-template.xlsx

# Demo
https://youtu.be/9OXAwAQ0xMc

# Project improvements
This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling. Also the model could be improved.
