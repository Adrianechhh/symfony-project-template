# Symfony template project

This template project includes configured and ready to use **PHP 8.3**, **MySQL 8.4**, **ClickHouse 24**, **Nginx**, **Redis** and **RabbitMQ** docker containers and **Symfony 6.4**
project files, created by ` composer create-project symfony/skeleton:"6.4.*" example-app` command. Nothing extra!

## Installation

To install and run this project follow next steps:

1. Create the **.env** file:
    ``` sh
    cp .env.example .env
    ````
   Set your own `GIT_EMAIL`,  `GIT_USER`, `APP_NAME` in the [.env](.env) file. You can also specify the project **name** and **description** at your [composer.json](composer.json).

2. Build containers:
    ``` sh
    docker-compose build
    ```
3. Run the containers and enter the php container:
    ``` sh
    docker-compose up -d && docker-compose exec php bash
    ```
4. Run composer install inside the container:
   ``` sh
   composer install
   ```
5. Run npm install inside the container:
   ``` sh
   npm install
   ```

### RabbitMQ Queue

The RabbitMQ Management panel can be accesed at http://localhost:15672/.
The **user** and **password** are specified in the [.env](.env) file.
