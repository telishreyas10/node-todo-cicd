
# DevOps CI/CD Project

Implemented a streamlined CI/CD pipeline using Jenkins, Docker, AWS, and GitHub. 

This project aims to automate code delivery, enhance collaboration, and ensure consistency in deployments. Key objectives include setting up Jenkins for automation, using GitHub for version control and connection to Jenkins using webhooks, Docker for containerization, Infrastructure as a Service (IAAS) Code for AWS resource management, and dynamic environments for testing and deployments.  


## Overview

- GitHub Repository:

    The project uses a forked GitHub repository as the source code repository. You can replace it with your own repository as needed.

    Steps to run todo app project : 

    ` npm install`
    
    `node app.js`

- AWS EC2 Instance:

    An EC2 instance is created on AWS using the Ubuntu t2 micro (free tier) image. This instance serves as the deployment target.

- Jenkins Setup:

    Jenkins, Docker.io, Node.js, and npm are installed on the EC2 instance to set up the CI/CD environment.

- Jenkins Pipeline:

    A Jenkins pipeline is configured, which consists of the following stages:

    Git Clone: Fetches the latest code from the GitHub repository.

    Docker Build: Builds Docker containers for the application.

    Docker Deploy: Deploys the application using Docker.
    
## Architecture

![Architecture](https://github.com/telishreyas10/node-todo-cicd/blob/master/assets/architecture.png)
## Contributions

Contributions are welcome! If you have any improvements or suggestions for this project, please feel free to open an issue or submit a pull request

