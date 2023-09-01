# exif-app-docker
This repository contains the docker compose file to set up containers for following EXIF web app services:
- Flask backend
- MongoDB server
- React frontend
## Setup
For security purposes, the MongoDB server is set up to be secured with an admin user. To facilitate this, in the repo root directory, ensure `.env` is present with the following fields:
```
MONGO_INITDB_ROOT_USERNAME=<your_username>
MONGO_INITDB_ROOT_PASSWORD=<your_password>
```
The backend container should use these same credentials to authenticate when connecting to the database container.
## Running Containers
Ensure the following repositories are present in this structure:
```
root_dir
├── exif-app-docker
│   
├── exif-app-backend
│
└── exif-app-frontend
```

To run the containers, navigate to `exif-app-docker` (where `docker-compose.yaml` is present), and run either:
- `$ docker compose up -d`
- `$ docker compose up --build -d` if changes have been made to a container's source code, or this is the first time building the containers

To stop the containers:
- `$ docker compose down`
