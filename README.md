# Dockerized MERN stack application 
![Animation](https://github.com/user-attachments/assets/a3b7a9ac-401c-4dd1-9846-a6cf252e5f70)


 ITI Supervisor: https://github.com/Ranaahmedit
 
### Create a network for the docker containers

`docker network create demo`

### Build the client 

```sh
cd mern/frontend
docker build -t mern-frontend .
```

### Run the client

`docker run --name=frontend --network=demo -d -p 5173:5173 mern-frontend`

### Verify the client is running

Open your browser and type `http://localhost:5173`

### Run the mongodb container

`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongodb:latest`

### Build the server

```sh
cd mern/backend
docker build -t mern-backend .
```

### Run the server

`docker run --name=backend --network=demo -d -p 5050:5050 mern-backend`

## Using Docker Compose

`docker compose up -d`


![Screenshot 2025-02-21 022656](https://github.com/user-attachments/assets/c315330f-158f-43ea-8ac0-2554124cb2c2)


#### Docker hub
https://hub.docker.com/repository/docker/mohamedashrf/project/general






