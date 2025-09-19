# A Project MERN stack With Docker🐳
<img width="1280" height="660" alt="image" src="https://github.com/user-attachments/assets/19c18cd4-a7f8-491a-8752-be2321ba215a" />


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

`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongo:latest`

### Build the server

```sh
cd mern/backend
docker build -t mern-backend .
```

### Run the server

`docker run --name=backend --network=demo -d -p 5050:5050 mern-backend`

## Using Docker Compose

`docker compose up -d`
<img width="458" height="194" alt="image" src="https://github.com/user-attachments/assets/4fa767f1-c6dc-49b6-bc06-5781654fde31" />


