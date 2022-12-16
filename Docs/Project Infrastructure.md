# Project Infrastructure

- The project features a full stack web app (Udagram) that utilizies AngularJS for the frontend and NodeJS for the backend.


- AWS services used:

    - RDS database was made on the AWS console to store API data using Posgres DB.
    - S3 bucket was made to host the frontend Angular App.
    - EB App was made using the eb cli to deploy the NodeJS API, commands that were used:
        - eb init: to initiazlie eb app instance for the API.
        - eb create: to create app environment.
        - eb deploy: to deploy the API initially.
        - eb health: to check the health of the environment.
        - eb logs: to check logs in case there is an error in deployment.


- Infrastructure Details

    - The backend runs through a RESTful NodeJS API which handles users' requests, the API is hosted on AWS elastic beanstalk.
    - The API communicates with a Postgres database to store user data such as account informations.
    - The DB utilizied by the API is hosted on an AWS RDS server for database CRUD operations.
    - Finally the frontend AngularJS app communicates to the API by making requests and awaiting responses.
    - The frontend app is hosted on AWS s3
    - Combining all AWS services, this full stack app can fully function.
    - Infrastructure Diagram shows this process graphically.


- An Infrastructure diagram can be found in Images/Diagrams to visualize the process.