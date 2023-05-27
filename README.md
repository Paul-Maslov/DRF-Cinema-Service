# Dockerizing DRF Cinema-Service

- Read the guideline before start

# Features:

- JWT autenticated;
- Admin panel /admin/;
- Documentation is located at /api/doc/swagger;
- Managing order and tickets;
- Creation movies with genres and actors;
- Creation cinema halls;
- Adding movie sessions;
- Filtering movies and movie sessions;

# Installation of Project:

### Install PostgreSQL and create db:

✨ Installation with Elephant (https://www.elephantsql.com/)

👉 Step 1 Register on site, chose TURTLE Tiny plan, create db 
          and receive necessary variables

👉 Step 2 After installation of the main programme put

``
POSTGRES_HOST="elephant server"

POSTGRES_NAME="elephant db name"

POSTGRES_USER="elephant user"

POSTGRES_PASSWORD="elephant password"
``

into file in the main root

``
.env
``

✨ To run PostgreSQL from Docker you can follow theese steps:

#### Step 1
👉  Install Docker: If you don't already have Docker installed on your system,
    you need to install it. Docker provides installation instructions for 
    different operating systems on their website:(https://docs.docker.com/get-docker/)

#### Step 2
👉 Pull the PostgreSQL Docker image: Open a terminal or command prompt and execute
   the following command to pull the official PostgreSQL Docker image from the Docker Hub:

``
docker pull postgres
``
