# AWS Continuous Integration Demo

# Project Overview:
This project showcases the implementation of continuous integration using AWS CodeBuild and AWS CodePipeline

# Prerequisites:
- AWS Account
- GitHub Account
- DockerHub Account

# Project Architecture:

![AWS CI Architecture Diagram drawio](https://github.com/veerababu558/AWS-Projects-001/assets/44125493/ac92d231-662f-4c39-8557-ddca53dff039)

## Steps:

## Creation AWS CodeBuild:
- Go to the AWS Management console and navigate to AWS CodeBuild
- Click on the “Create Project Button”.
- Provide the name of your Build Project.
- Select source as GitHub and connect to your GitHub and provide the name of your GitHub Repository.
- Configure the Build environment such as Provisioning model , Environment  image, Compute and Operating required for the application.
- Specify the build command required for Python application such as installing dependencies and artifacts etc.
- Make sure IAM service role to have access Systems manager policy as Buildspec file is referring Docker user name and pwd from Systems manager.


## Creation of AWS CodePipeline:
- Go to the AWS management console and navigate to AWS CodePipeline.
- Click on the “Create pipeline” button.
- Provide the Pipeline name.
- For source stage select “GitHub Version 2” as Source provider.
- Connect to your GitHub account and provide the GitHub repo name and branch as Main.
- For Build stage select “Code build”  as Build provider.
- Click on the “Skip build stage” button.
- Click on the “Create Pipeline” button.


Now, AWS CodeBuild and CodePipeline have been set up successfully.

## Project Execution

After making changes to the app.py file, AWS CodePipeline is automatically triggered, subsequently triggering AWS CodeBuild to build the Docker image and push it to Docker Hub.
Below is the screenshot showing that AWS CodePipeline has been triggered and completed successfully.

![AWS CI ScreenShots drawio](https://github.com/veerababu558/AWS-Projects-001/assets/44125493/f4bc08a8-ae25-4433-9222-f95091400957)








