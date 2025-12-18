🚀 Run the Application Using Docker Compose
Prerequisites

Docker installed

Docker Compose installed

Verify installation:

docker --version
docker compose version

Steps to Run the Application

Clone the repository

git clone https://github.com/Ehshanulla/containerized_capstone_project



Build and start all services

docker-compose up -d


(or, for newer Docker versions)

docker compose up -d


Access the application

Open your browser and visit:

http://localhost

Stop the application
docker-compose down


### Services
- Frontend: Angular + Nginx (Port 80)
- Backend: Spring Boot (Port 8080)
- Database: MongoDB

### Default URLs
- Frontend: http://localhost
- Backend API: http://localhost/api

✔ Matches Docker standards
✔ Zero confusion during evaluation
