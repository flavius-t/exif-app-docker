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
To run the containers, ensure you are in the repo root directory (where `docker-compose.yaml` is present), and run either:
- `$ docker compose up -d`
- `$ docker compose up --build -d` if changes have been made to a container's source code

To stop the containers:
- `$ docker compose down`
