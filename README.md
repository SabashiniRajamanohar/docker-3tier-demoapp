# Node.js User Registartion App with MongoDB and MongoDB Express using Docker Conatiners

This Project is a Dockerized full-stack  application that allows users to register with a email, username , and password via a 
node.js backend and a simple frontend form.

---

## Feartures

- simple frontend form for user registration
- Node.js + Express backend to handle form submissions
- MongoDB for data storage
- Mongo Express as a web-based MongoDB admin interface
- Fully containerized using Docker
- Easy setup and teardown with Docker compose


---

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongo Express 
- Docker & Docker Compose

---

## Getting Started

### Prerequisties

- [Docker] (https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

---

### How to run the project

1. Clone this repository (if you haven't already):
2. 
   ```bash
   git clonegit@github.com:SabashiniRajamanohar/docker-3tier-demoapp.git
   
3. Ensure the following file exist
   - Dockerfile -> for building the docker image **node.js** to run on docker containers
   - docker compose.yaml -> To define run all the services(node.js, MongoDB, Mongo Express) on Containers

4. Run the following Command to build and start the containers.
   ```bash
   docker build -t node.js
   docker compose -f compose.yaml up 

5. Ports Running:
   - node.js exposed on port  5050 (Backend Server)
   - MongoDB running on 27017 (Database for storing the user data)
   - Mongo Express running on 8081 (Web UI to view MongoDb collections)

### How it works ###

. The user fills out a profile form (email, usernmae, password).
. On submission, the data is sent to the Node.js backend.
. The backend stores the data in MongoDB.
. You can view the stored data in MongoDB
Express at http://localhost:8081 , inside the database **demo-db** and collection **infos**

### Volumes ###
. A named volume (mongo-db) is created for MongoDB to persist data.
. An additional Volume is ampped for /tmp in Mongo Express to avoild auto-created anonymous volumes

### Stopping the Application ###
 To stop and remove all containers.

 ```bash
 docker compose -f compose.yaml down

### Project Summary ###

This project is a containerized Node.js user registration form application that runs with Docker and Docker Compose. It includes three services: a Node.js backend(built from a custom docker file), a MongoDB database to store user data, and Mongo Express as a web-based MongoDB GUI. Docker Compose orchestrates these services, making it easy to run the full stack with one command. Users can submit their information through the form, which is saved in MongoDB and can be viewed in real-time using Mongo Express. This setup demonstrates how to develop and deploy a simple full stack app usinh Docker Containers
