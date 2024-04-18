# Docker Compose Laravel Environment

## Description

This Docker Compose setup includes:

- Laravel Application
- Nginx
- MySQL
- Random HTTP Docker Image

## Environment Setup

### Prerequisites

Make sure you have Docker and Docker Compose installed on your machine.

- Docker: [Installation Guide](https://docs.docker.com/get-docker/)
- Docker Compose: [Installation Guide](https://docs.docker.com/compose/install/)

### Clone the Repository

bash
git clone https://github.com/jd2024-thiio.git
cd jd2024-thiio

Database Configuration
The MySQL database is configured with the following credentials:

Database: mydatabase
Username: root
Password: rootpassword
You can connect to the database using any MySQL client with these credentials.

Laravel Configuration
The Laravel application is pre-configured to use the MySQL database. The database configuration can be found in the .env file inside the laravel directory.


#Build and Run
docker-compose up --build
#Or to start the random HTTP service:
docker-compose --profile random up --build
Access the Application
Laravel Application: http://devops.test
Random HTTP Docker Image at /thiio: http://devops.test/thiio


Make sure to replace `jd2024-thiio` with the actual name of your repository.


Running Tests
Laravel Tests
To run the Laravel tests, you can use the following command:
docker-compose exec laravel ./vendor/bin/phpunit

Random HTTP Docker Image Tests
If you want to test the random HTTP Docker image, you can use curl or any HTTP client to send requests to http://devops.test/thiio.

Example with curl:
curl http://devops.test/thiio

Clean Up
To stop and remove all containers, networks, and volumes:
docker-compose down -v



You can place the `docker-compose.yml`, `nginx.conf`, `Dockerfile`, and `README.md` in the root directory of your project.
