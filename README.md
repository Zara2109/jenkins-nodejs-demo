# Jenkins CI/CD Pipeline

## Overview
A simple CI/CD pipeline using Jenkins and Docker to automate the build, test, and deployment of a Node.js application.

## Tools Used
- Jenkins
- Docker
- GitHub
- Node.js
- AWS EC2

## Workflow

```text
GitHub → Jenkins → Build → Test → Deploy
```

1. Code is pushed to GitHub.
2. Jenkins detects changes and triggers the pipeline.
3. Docker builds the application image.
4. Tests are executed.
5. The application is deployed as a Docker container.

## Pipeline Stages

### Build
```bash
docker build -t jenkins-demo .
```

### Test
```bash
npm test
```

### Deploy
```bash
docker run -d --name jenkins-demo -p 3000:3000 jenkins-demo
```

## Learning Outcomes
- Jenkins Pipeline Creation
- CI/CD Fundamentals
- GitHub Integration
- Docker Container Deployment
- Automated Build, Test, and Deploy Process

## Outcome
Successfully implemented a Jenkins-based CI/CD pipeline that automatically builds, tests, and deploys a Node.js application.