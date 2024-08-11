# Docker PHP

## Description

This project provides a development environment for a PHP application using Docker Compose. It includes the following services:

* nginx: A reverse proxy server for routing traffic to the PHP application.
* php: Built from a Dockerfile that installs required dependencies and sets up PHP-FPM.
* mysql: A database server to store application data.
* phpmyadmin (optional): A web-based interface for managing the MySQL database.

## Prerequisites

* Docker: https://docs.docker.com/desktop/install/mac-install/
* Docker Compose: https://docs.docker.com/compose/install/  


## Getting Started

1. **Clone the repository:**

   ```bash
   git clone [https://github.com/jakhongirikromidinov/docker-php.git]  
2. ***Create .env file (optional):***
    To override the default MySQL root password, create a file named .env in the project root directory with the following content:

   ```
   MYSQL_ROOT_PASSWORD=your_desired_password
   ```
   Important: Do not commit the .env file to version control.

3. ***Build and start the services:***
   ```bash
   docker-compose up -d
   ```
   This command will build the application image (if necessary), create and start all containers defined in the docker-compose.yml file in detached mode (-d).

4. ***Access the application:***
* Web application: Open your web browser and navigate to http://localhost. You should see the default PHP page or your application's content, depending on your project setup.
* phpMyAdmin (optional): Access the phpMyAdmin interface by opening http://localhost:1500 in your browser (assuming you included the phpmyadmin service). The default credentials are PMA_HOST=mysql and the password you set in the .env file (or root if no .env file is present).
