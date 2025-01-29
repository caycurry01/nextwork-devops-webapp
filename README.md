# Java WebApp on AWS EC2 with GitHub Integration and CI/CD

### This project demonstrates the development and deployment of a **basic Java web application** hosted on an **AWS EC2 instance**, with version control managed via **GitHub** and CI/CD pipelines for automated deployment.
---

## Overview

This project focuses on:
1. Building a simple Java web app.
2. Deploying the app to an **AWS EC2 instance**.
3. Integrating **GitHub** for version control and **CI/CD** for automation.

It uses a single branch workflow (`main` branch) to streamline development, with a focus on demonstrating fundamental DevOps principles.

---

## Features
- **Java-based web application** with basic functionality.
- Hosted on an **AWS EC2 instance** for high availability.
- Continuous deployment enabled via **GitHub Actions**.
- Codebase managed and edited in **VS Code**.

---

## Technologies Used
- **Java**: Programming language for application development.
- **Apache Maven**: Build and dependency management tool.
- **AWS EC2**: Hosting the web app.
- **Git/GitHub**: For version control.
- **GitHub Actions**: For automating CI/CD pipelines.
- **VS Code**: IDE used for development.

---

## Development Process

1. **Initialize Git**:
   - Run `git init` to set up the repository and create a branch (`main`).
   - Push the project to a new GitHub repository for version control.

2. **Edit in VS Code**:
   - Make changes to the Java codebase and test locally.

3. **Automate Deployment**:
   - Use GitHub Actions to trigger CI/CD pipelines for testing, building, and deploying the application whenever changes are pushed to the repository.

---

## Deployment

1. **AWS EC2 Instance Setup**:
   - Launch an EC2 instance with a Linux distribution.
   - Install necessary tools (Java runtime, Maven, etc.).
   - Configure security groups to allow web traffic (port 80/443).

2. **CI/CD Integration**:
   - Push changes to the GitHub repository.
   - GitHub Actions pipeline automates:
     - Building the Java app (`mvn clean package`).
     - Deploying the app to the EC2 instance using SCP/SSH.

---

## Setup and Installation

### Prerequisites
- AWS account with an EC2 instance set up.
- SSH key pair for accessing the EC2 instance.
- Git installed locally.
- Java Development Kit (JDK) installed.
- GitHub repository created.

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/repository-name.git
   cd repository-name
   ```

2. Make changes to the application code in VS Code.

3. Push changes to GitHub:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

4. Set up the GitHub Actions pipeline for automated builds and deployment.
