# Pipeline Process

- Pipelining process steps:

    - AWS was configured to host the full stack app.
    - A repo was made on github to store the code of the project.
    - CircleCI was connected to the github account and the project was set up on CircleCI.
    - Environment Variables were added to CircleCI for a smooth deployment pipeline.
    - Pipelining Config was adjusted to implement the Udagram workflow which does two main jobs: (documented in Images/CircleCI)
        - Building the app.
        - Deploying the app.



- How the pipeline works.

    - The develpoer writes code changes in the project.
    - push the changes to github repositry using git.
    - The git push triggers a pipeline workflow execution in CircleCI (because CircleCI is linked to github).
    - The Pipeline workflow runs scripts to do certain jobs.
    - The pipeline workflow ends by running deployment scripts that contact the AWS CLI through IAM users authentication through environment variables.
    - Code is updated on AWS as a result of the workflow.
    - The process is repeated throughout the developement life-cylce of the project.

- A pipeline diagram can be found in Images/Diagrams to visualize the process.