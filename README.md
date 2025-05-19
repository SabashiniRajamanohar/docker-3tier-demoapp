# Node.js User Registartion App with MongoDB and MongoDB Express using Docker Conatiners

This Project is a Dockerized full-stack  application that allows user to register with a email, username , and password via a 
node.js frontend

---

## Feartures

- Node.js frontend for user registration
- MongoDB for data storage
- Mongo Express as a web-based MongoDB admin interface
- Fully containerized using Docker
- Easily setup and teardown with docker compose

---

## Technologies Used

-  Node.js
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

1. ** **
2. Start the application

docker compose -f compose.yaml up

This Command will 
. Build the Node.js frontend using your Docker file

. Pull the official MongoDB and Mongo express images

. Start all three conatiners (Node.js app, MongoDB, Mongo express)

### After Registration ###

After submitting the registration form, the data is stored in the MongoDB database under the users collection

