🚀 Enterprise DevSecOps CI/CD Pipeline with GitHub Actions

This project demonstrates a complete enterprise-style DevSecOps CI/CD pipeline built using GitHub Actions, Docker, Trivy, and Gitleaks for a Node.js application.

The pipeline automates code validation, security scanning, containerization, registry publishing, and runtime verification — following real industry CI/CD practices.

📌 Project Objective

To design and implement a realistic enterprise CI/CD pipeline that:

Ensures code quality

Enforces security checks

Automates Docker image creation

Publishes images to DockerHub

Validates application runtime behavior

This project focuses on CI + DevSecOps + Container workflow.

🏗️ Pipeline Architecture
Push to main branch
        ↓
CI Job (Build & Test)
        ↓
Security Scan (Trivy + Gitleaks)
        ↓
Docker Build
        ↓
Docker Push to Registry
        ↓
Runtime Container Validation
        ↓
Container Cleanup

🔧 Tech Stack

Node.js

GitHub Actions

Docker

DockerHub Registry

Trivy (Vulnerability Scanning)

Gitleaks (Secret Detection)

YAML

📁 Project Structure
.
├── app.js
├── test.js
├── package.json
├── Dockerfile
└── .github
    └── workflows
        └── cicd.yml

⚙️ CI/CD Workflow Overview

The pipeline is triggered automatically on every push to the main branch.

🔹 CI Stage

Checkout repository

Setup Node.js environment

Install dependencies

Run tests

🔹 Security Stage

Trivy filesystem scan

Gitleaks secret detection

🔹 Docker Stage

Build Docker image

Login to DockerHub using secure tokens

Push image to DockerHub registry

🔹 Runtime Validation Stage

Pull Docker image

Run container inside CI runner

Validate application using HTTP request

Stop and clean up container

🔐 Secrets Used

GitHub Actions secrets:

Secret Name	Purpose
DOCKER_USERNAME	DockerHub username
DOCKER_PASSWORD	DockerHub access token
🧠 Why This Project Is Enterprise-Grade

This pipeline follows real DevOps principles:

Job isolation using needs

Secure authentication with tokens

Registry-based artifact storage

Runtime verification

Security-first design

No hard-coded secrets

CI machine independence

🧪 Runtime Validation

The pipeline verifies the container by:

curl http://localhost:3000


If the application does not respond correctly, the pipeline fails automatically.

🚀 Future Improvements

Kubernetes deployment stage

Versioned Docker tagging

Artifact uploads

Multi-environment pipelines

Production deployment strategies

📖 Learning Outcomes

Through this project, I learned:

CI/CD pipeline design logic

Docker image lifecycle

Registry-based workflows

Job dependency chaining

DevSecOps integration

CI authentication mechanisms

Runtime container validation

🏆 Resume Line

Designed and implemented an enterprise-grade DevSecOps CI/CD pipeline using GitHub Actions, Docker, Trivy, and Gitleaks with automated container validation.

🙌 Author

Gaurav Banik
DevOps Learner | CI/CD | DevSecOps | GitHub Actions | Docker
