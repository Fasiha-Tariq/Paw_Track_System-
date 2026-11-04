# Paw_Track_System-
A team of Web developers, working on a Pet Adoption and Fostering System, named as Paw_Track

# Group Memebers
1. Urba Naseem - Group Leader
2. Shiza Shahid - Collaborator #01
3. Syeda Ayesha Fatima - Collaborator #02
4. Fasiha Tariq - Collaborator #03
5. Khansa Noor - Collaborator #04

# Deliverable - 1 
1. Created a basic home.html file
2. pushed on Git
3. Cloned by contributors
4. Contributors changes pushed to their respective branches
5. All the commits were merged into the main branch by the leader

# Deliverable - 2 (Building and Running  Docker Images)
1. Create a Docker file
2. Build the docker image
command : docker build --tag devops .
3. Run the docker image
command : docker run -d -p 8080:80 devops:latest  

# Deliverable - 3 (Added Backend Module and Created Docker-comper file)
1. Created Docker file for the Backend module
2. Created docker-compose.yml  
3. Application is run through the Docker compose

# Activity 2
Making changes in the README.md file to test the jenkins software 

# Change 2
Again just making minor change in the README file to generate build 2 in jenkins


# Project Deliverable 4 - Automating CI/CD Pipeline

## CI/CD Pipeline Overview
This repository utilizes a GitHub Actions CI/CD pipeline triggered automatically on pushes to the `main` branch, merged pull requests, or manual execution (`workflow_dispatch`). The workflow builds multi-container Docker images for both the frontend and backend, pushes the tagged images to Docker Hub, and automatically deploys the latest version to an AWS EC2 instance over SSH.

## How to Run & Deploy Locally
1. Prerequisites: Install Docker and Docker Compose.
2. Build and start the containers:
```bash
docker compose up --build -d
```
3. Access the application:
* **Frontend:** `http://localhost:3000`
* **Backend API:** `http://localhost:5000`

## Changelog
* **v1.0.0 (Deliverable 4):**
* Configured multi-container directory layout.
* Prepared project for GitHub Actions CI/CD integration (`.github/workflows/ci-cd.yml`).
* Added initial pipeline documentation and setup guide.
