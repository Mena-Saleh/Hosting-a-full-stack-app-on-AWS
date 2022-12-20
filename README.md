# Hosting a full stack application

## Table of Contents

1. Project Description 
2. Project Steps Documentation
3. Dependencies
4. Scripts and Instructions
5. Copyrights And Acknowledgements

## Project Description 

This project demonstrates and documents the hosting process of an already provided full stack web application. The web app is called Udagram, it runs a NodeJS API and a frontend that is made with AngularJS. This project utilizes AWS to host the application. EB, RDS and S3 were used to host and deploy this app. Pipeling was done with CircleCI to make the deployment process automated and headache free

- The website can be accessed on the following link: http://udagram-angular3416.s3-website-us-east-1.amazonaws.com (currently down)

- NOTE: Images documenting success of each and every step can be found in the Images folder (AWS - CircleCI - Diagrams).

- NOTE: in the Docs folder, three structured documents document the following: Project Infrastructure, App Dependencies and Pipeline Process in more details.

## Project Steps Documentation



- Steps followed in the making of this project:

    - RDS database was made on the AWS console to store API data.
    - S3 bucket was made to host the frontend Angular App.
    - EB App was made using the eb cli to deploy the API, commands that were used:
        - eb init: to initiazlie eb app instance for the API.
        - eb create: to create app environment.
        - eb deploy: to deploy the API initially.
        - eb health: to check the health of the environment.
        - eb logs: to check logs in case there is an error in deployment.
    - A repo was made on github to store the code of the project.
    - CircleCI was connected to the github account and the project was set up on CircleCI.
    - Environment Variables were added to CircleCI for a smooth deployment pipeline.
    - Pipelining Config was adjusted to implement the Udagram workflow which does two main jobs: (documented in Images/CircleCI)
        - Building the app.
        - Deploying the app.
    - Project is commited and pushed to github using git, which triggers a CircleCI workflow which deploys the app on AWS.

## Dependencies And About The Project

- Amazaon Web Services Dependencies/Components:

    - Elastic Beanstalk (EB)
    - Simple Storage Service (S3)
    - Relational Database Service (RDS)
    - Identity and Access Management (IAM)

- Pipelining Dependencies:

    - CircleCI
    - Git
    - Github

- Project Specific Dependencies:

    - NodeJS (Packages listed in package.json)
    - AngularJS (Packages listed in package.json)
 

## Scripts and Instructions

- Root level scripts:

    - These scripts can be found in the package.json file that is in the root directory of the repositry.
    - They are made to provide some sort of abstraction to the proccess, where they call other scripts that are found in the API and the frontend.
    - These scripts are directly invoked in the CircleCI config.yml file for convenience, because they are more clean and refined.
    - Scripts:

        "frontend:install": install frontend packages.
        "frontend:start": start the Angular app locally.
        "frontend:build": build the app in the www folder.
        "frontend:test": run tests on the frontend app.
        "frontend:e2e": run end point tests.
        "frontend:lint": run a linter.
        "frontend:deploy": deploy the app to s3.

        "api:install": install backend packages.
        "api:build": build the API in the www folder.
        "api:start": run the API locally
        "api:deploy": deploy the API to eb.

        "deploy":  deploy both frontend and backend
    }

- udagram-api scripts:

    - Can be found in the package.json file in udagram-api folder.
    - Scripts specific to the API:

        - "start": start the transpiled API code (production).
        - "tsc": buils the API.
        - "dev": start the typescript code (development)
        - "clean": cleans the project.
        - "deploy": deploys API to AWS eb
        - "build": builds the API after cleaning and installing packages.


- udagram-fronted scripts:

    - Can be found in the package.json file in udagram-frontend folder.
    - Scripts specific to the frontend Angular App:

       - "ng": Generates angular workspace
       - "start": Runs the angular app.
       - "build": Builds production code in www folder.
       - "deploy": Deploys the Angular App to S3.
       - "test": Runs tests on the app.
       - "lint": Runs a linter.
       - "e2e": Runs end to end testing.



## Copyrights And Acknowledgements

    The code for this project was provided by Udacity and I do not own any of it. The only task that was done by me is the deployment process of the application using AWS and CircleCI for pipelining and automation.

    - About The Author
        - Name: Mena Ashraf Mikhael Saleh
        - Email: Mena.a.saleh.2001@gmail.com
        - GitHub: https://github.com/Mena-Ibrahim
        - LinkedIn: https://www.linkedin.com/in/mena-saleh-23b947167/


