# SRE Student API

Inspired by the exercise from the [SRE Bootcamp](https://playbook.one2n.in/sre-bootcamp/sre-bootcamp-exercises/1-create-a-simple-rest-api)

## Project Architecture and Design Strategy
The project is based on the **Hexagonal Architecture** organized with packaged not modules.

## Functional Requirements
- Add a new student.
- Get all students.
- Get a student with an ID. 
- Update existing student information. 
- Delete a student record.

## Running This Project

### Prerequisites

Before running this project, ensure that you have the following installed:

- Java 17
- Maven (for building and managing dependencies)
- Docker installed on your system. You can download and install Docker from [here](https://www.docker.com/products/docker-desktop).

### Getting Started

Follow these steps to get the project up and running on your local machine:

1. **Clone the Repository**:
   ```shell
   git clone https://github.com/jonamarkin/student-management-api.git
   cd student-management-api
   
2. **Build The Project**
    ```shell
   mvn clean install
   
3. **Run The Project**
    ```shell
   mvn spring-boot:run

### Using MakeFile
Alternatively you can simply make use of the **Makefile** to start the project by running the following command in the root directory
```shell
make run
```

## Accessing The API

1. You can access the Swagger documentation of the API Via
   ```shell
   http://localhost:8080/swagger-ui/index.html
   ```
2. [Postman Documentation](https://documenter.getpostman.com/view/26444770/2sA2xiWrmY)
   

## Database
This project uses PostgreSQL Database.

## Running DB Migrations
```shell
make migrate-db
```

## Building and Running With Docker Compose

To build the Docker image, run:

```bash
docker-compose up --build
```

## Accessing The Application
Access the running application at http://localhost:8080

## MakeFile Common Tasks
The project contains a Makefile which simplifies performing certain common tasks.
Find below handy commands that may be helpful
- `make build`: Build all Docker images
- `make run-db`: Start only the PostgreSQL Database
- `make migrate-db`: Run database migrations
- `make build-api`: Build the API Docker Image
- `make run-api`: Start the API container

## Alternative Way Of Starting The Application
With the available Makefile commands, another way of starting the application will be the run the command:
```shell
make run-api
```
This will ensure database is running and migrations are applied and start the application.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests to make improvements.