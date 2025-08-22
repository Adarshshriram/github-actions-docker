# github-actions-docker

CI/CD Pipeline with GitHub Actions & Docker
.
# Project Overview

## This project demonstrates how to set up a CI/CD pipeline using GitHub Actions to:

- Build a Docker image for a Node.js app
- Push the image to Docker Hub
- Automate builds on every code push
- Optionally run locally with Docker / Minikube

This is a resume-worthy DevOps project showing skills in CI/CD, Docker, and GitHub Actions.

# Tools & Technologies

- GitHub Actions – CI/CD automation
- Docker – Containerization
- Docker Hub – Image registry
- Node.js – Sample application

# Repository Structure

- .github/workflows/docker-image.yml   # CI/CD pipeline definition
- Dockerfile                           # Docker build instructions
- app.js                               # Simple Node.js app
- package.json                         # Dependencies and scripts
- README.md                            # Documentation

# Workflow (GitHub Actions)

- Trigger: On every push to main branch

- Steps:

   - Checkout source code
   - Login to Docker Hub
   - Build Docker image
   - Push image to Docker Hub

# Setup Instructions

1. Clone the Repository

- git clone https://github.com/<username>/github-actions-docker.git
- cd github-actions-docker

2.  Create Docker Hub Secrets in GitHub

- Go to GitHub Repo → Settings → Secrets → Actions

 - Add:

  - DOCKER_USERNAME 

  - DOCKER_PASSWORD 

3.  Push Code to GitHub

- git add .
- git commit -m "Initial CI/CD pipeline project"
- git push origin main

4.  Verify in Actions Tab

- Go to GitHub → Actions

- Check if the workflow runs successfully

- Confirm Docker image is pushed to Docker Hub

5. Run Locally

- Pull the Docker image from Docker Hub:

  - docker pull adhiadarsh/myapp:latest

  - docker run -d -p 3000:3000 adhiadarsh/myapp:latest

  - Open in browser: 👉 http://localhost:3000

6. Screenshots to Add in README

 -  GitHub Actions workflow running (green build)

   <img width="940" height="484" alt="image" src="https://github.com/user-attachments/assets/7484b9cb-93ea-44b9-8719-305186d0e5e3" />


 -  Docker Hub repo showing pushed image

   <img width="940" height="469" alt="image" src="https://github.com/user-attachments/assets/ecdec76a-9b9e-47ae-8ced-ce9ec410f1d8" />


 -  App running locally in browser

   <img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/d96fea09-f559-4259-820b-75c716c0c666" />


7. Outcome / Learnings

- Hands-on CI/CD with GitHub Actions

- Automated Docker image builds & pushes

- Integration of GitHub + Docker Hub

- End-to-end deployment pipeline
