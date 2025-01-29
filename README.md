# Java WebApp on AWS EC2 with GitHub Integration and CI/CD  

### This project demonstrates the development and deployment of a Java web application hosted on an AWS EC2 instance. Version control is managed via GitHub, and CI/CD automation is handled using AWS CodePipeline, CodeBuild, and CodeDeploy.

## Overview  

This project focuses on:  
- **Building** a simple Java web application.  
- **Deploying** the app to an AWS EC2 instance.  
- **Integrating** GitHub for version control and AWS CI/CD for automation.  
- **Using AWS native services** instead of GitHub Actions for deployment.  

## Features  
- Java-based web application with basic functionality.  
- Hosted on an AWS EC2 instance for high availability.  
- Continuous deployment enabled via AWS CodePipeline.  
- Codebase managed and edited in VS Code.  

## Technologies Used  
- **Java**: Programming language for application development.  
- **Apache Maven**: Build and dependency management tool.  
- **AWS EC2**: Hosting the web app.  
- **Git/GitHub**: For version control.  
- **AWS CodePipeline**: Manages CI/CD automation.  
- **AWS CodeBuild**: Builds and packages the application.  
- **AWS CodeDeploy**: Deploys the application to EC2.  
- **VS Code**: IDE used for development.  

## Development Process  

### 1. **Initialize Git**  
Run the following commands to set up the repository:  
```bash
git init  
git add .  
git commit -m "Initial commit"  
git push origin main  
```

### 2. **Edit Code in VS Code**  
Modify the Java application and commit changes.  

### 3. **Automated Deployment via AWS CI/CD**  
Instead of GitHub Actions, the CI/CD pipeline is handled by AWS services:  

- **AWS CodePipeline**: Automatically triggers on GitHub updates.  
- **AWS CodeBuild**: Builds the project using `mvn clean package`.  
- **AWS CodeDeploy**: Deploys the built package to an EC2 instance.  

## Deployment Setup  

### 1. **AWS EC2 Instance Setup**  
- Launch an EC2 instance with a Linux distribution.  
- Install required dependencies (Java runtime, Maven, AWS CLI).  
- Configure security groups to allow web traffic (ports 80/443).  

### 2. **AWS CodePipeline Setup**  
- Connect GitHub as the source repository.  
- Configure CodeBuild to build the project.  
- Store artifacts in an S3 bucket.  
- Use CodeDeploy to deploy the application to EC2.  

## Setup and Installation  

### Prerequisites  
- AWS account with an EC2 instance set up.  
- IAM role with permissions for CodePipeline, CodeBuild, and CodeDeploy.  
- SSH key pair for accessing the EC2 instance.  
- Git and Java Development Kit (JDK) installed.  
- GitHub repository created.  

### Steps  
#### Clone the repository:  
```bash
git clone https://github.com/your-username/repository-name.git  
cd repository-name  
```
#### Make changes in VS Code  

#### Push changes to GitHub:  
```bash
git add .  
git commit -m "Update application"  
git push origin main  
```

Once the changes are pushed, AWS CodePipeline will handle the rest, automatically building and deploying the application.
