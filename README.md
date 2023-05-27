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

#### Step 1
👉 Register on site, chose TURTLE Tiny plan, create db 
   and receive necessary variables

#### Step 2
👉 After installation of the main programme put

``
POSTGRES_HOST=<elephant server>
POSTGRES_NAME=<elephant db name>
POSTGRES_USER=<elephant user>
POSTGRES_PASSWORD=<elephant password>
``

into file  ``.env``  in the main root

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

#### Step 3
👉  Create a Docker container for PostgreSQL: Once the image is pulled, 
    you can create a Docker container to run PostgreSQL. 
    Use the following command:

``
docker run --name my-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
``

👉  Verify the PostgreSQL container: You can check if the PostgreSQL 
    container is running by executing the following command:

``docker ps``

### Installing application from GitHub:

#### Step 1

``
git clone git@github.com:Paul-Maslov/DRF-Cinema-Service.git
cd DRF-Cinema-Service
python -m venv venv
venv/Scripts/activate
pip install -r requirements.txt
``
#### Step 2
👉  Set to ``.env``

``
POSTGRES_HOST=<your db host name>
POSTGRES_NAME=<your db name>
POSTGRES_USER=<your db username>
POSTGRES_PASSWORD=<your db password>
``

#### Step 3

``
python manage.py migrate
python manage.py runserver
``

### Run with Docker

Docker should be installed

``
docker-compose build
docker-compose up
``

### Getting Acsess

- create user via ``/api/user/register``
- get access token via ``api/user/token``

