# CI/CD Configurations

This repository contains the configuration files and scripts to set up a robust CI/CD pipeline. The pipeline automates building, testing, and deploying applications to a cloud instance.

## Repository Structure

```
├── circleci              # CircleCI workflows
├── github-actions        # Github actions workflows
├── gitlab-ci             # GitLab CI/CD configurations
├── dockerfiles           # Docker-related configurations
└── README.md             # Documentation
```
<p align="center"><a href="https://ibb.co/kgdF9Vf"><img src="https://i.ibb.co/LzGfJDW/CICD-Pipeline-Demystifying-The-Complexities-1.png" alt="CICD-Pipeline-Demystifying-The-Complexities-1" border="0"></a></p>

## Key Features

- **Automated Build and Test**: Ensure every commit is tested and built.
- **Dockerized Deployment**: Applications are containerized for consistency.
- **Cloud Deployment**: Automated deployment to a cloud instance.

## Prerequisites

Before setting up this pipeline, ensure you have:

1. A cloud provider account with a cloud instance configured.
2. Docker installed on your local machine and a cloud instance.
3. Necessary environment variables configured such as:
   - `CLOUD_RESOURCE_ACCESS_KEY_ID`
   - `CLOUD_RESOURCE_SECRET_ACCESS_KEY`
   - `CLOUD_RESOURCE_INSTANCE_IP`
   - `DOCKER_USERNAME`
   - `DOCKER_PASSWORD`

## Workflows

### Build and Test Workflow

This workflow:

1. Builds the application Docker image.
2. Run tests to ensure code quality.

### Deployment Workflow

This workflow:

1. Pushes the Docker image to a container registry.
2. Connects to the EC2 instance via SSH.
3. Pull the latest image and restart the application.

### Author

Implemented by [Sadeesha Perera](https://github.com/SadeeshaPerera)

For questions or feedback, feel free to reach out!
