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

# Deliverable - 4 (Automating CI/CD Pipeline)
## 1. Description of CI/CD Pipeline
This project uses a GitHub Actions CI/CD pipeline defined in `.github/workflows/ci-cd.yml`.

**Trigger:** Runs automatically on pushes to `main` or when a pull request is merged into `main`.
**Build & Push:** Authenticates with Docker Hub using repository secrets, builds the backend and frontend Docker images, and pushes them to Docker Hub (`fasiha21`).
**Deploy:** Connects to our AWS EC2 instance over SSH, pulls the images, and restarts the containers automatically.

**Pipeline stages:**
1. Checkout code
2. Log in to Docker Hub (secret-based)
3. Build `paw-track-backend` and `paw-track-frontend` images
4. Push both images to Docker Hub (`:latest` and `:<git-sha>`)
5. SSH into EC2 → `docker compose pull` → `docker compose up -d`

## 2. Instructions to Run and Deploy the App

### Local run with Docker Compose
```bash
docker-compose up --build -d
