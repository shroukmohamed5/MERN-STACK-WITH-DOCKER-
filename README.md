# A Project MERN Stack With Docker🐳
<img width="1280" height="660" alt="image" src="https://github.com/user-attachments/assets/19c18cd4-a7f8-491a-8752-be2321ba215a" />

<img width="1915" height="401" alt="image" src="https://github.com/user-attachments/assets/1583724a-a9f5-4720-b49c-aaca218e1c73" />


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


<img width="962" height="89" alt="image" src="https://github.com/user-attachments/assets/9052de75-6c1d-421f-b80d-568dff92ffd4" />






