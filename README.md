# Create a Web API and database with Spring
[![web](https://img.shields.io/static/v1?logo=heroku&message=Online&label=Heroku&color=430098)](https://spring-web-api-assignment.herokuapp.com/swagger-ui/index.html)

This project was an assignment with the end-goal being to create and deploy a REST Web API and PostgreSQL database with Spring in Heroku.

## Background
For this assignment we were required to make an app using Spring in Java with different dependencies mentioned in "Built With".
The database is build from the ground up using PostgreSQL and implements seeder data on application start. We used Java to create a REST API and documented it with Swagger and Postman.

## Installation

### Local

Requirements:
 - IntelliJ or similar IDE
 - Docker
 - Postman (optional)

1. Download or clone repository to a local folder.
2. Start up Docker 
3. Run the following command in a terminal

```bash
docker run -d --name moviesdb -e POSTGRES_PASSWORD=supersecretpassword -e POSTGRES_DB=moviedb -p 5432:5432 postgres:14-alpine
```

4. Open the downloaded or cloned repository in your IDE
5. Run the app
6. Navigate to http://localhost:8080/swagger-ui/index.html#
7. Alternative to 6: 
Import the Assignment3_WebApi_And_Database.postman_collection.json from the resources folder in Postman
8. Start testing the endpoints

## How To Use

### Entity information
The assignment required us to create a Franchise, Character and Movie entity. Since Character is already a Java class we chose Actor as a replacement for the Character entity class.

### API Endpoints - SwaggerIO
When the application loads up you will see the swagger interface. Here you can test the different endpoints, and we would like to give some pointers for getting the correct responses.

#### PUT Endpoints
For every PUT endpoint which points to updating a certain franchise, movie or actor. <br />
Please leave the relation arrays for example: "actors": [  "String" ] EMPTY as following: "actors": [] or remove the field entirely. <br />
In the same request body you need to set the "franchise" to NULL unless you know any of the other franchises id described in the database.

#### POST Endpoints
For every POST endpoint which points to creating a certain franchise, movie or actor. <br />
Please remove the "id" field entirely from the request body and follow the same guideline as stated for the PUT Endpoints and leave relation arrays empty.

### API Endpoints - Postman
In the application resources folder a JSON API testcollection (Assignment3_WebApi_And_Database.postman_collection.json) has been added for testing the endpoints in Postman. These tests can be run as is.

## Built With
[IntelliJ IDEA](https://www.jetbrains.com/idea/)

[Spring Framework](https://spring.io/)
 - [Spring Data JPA](https://spring.io/projects/spring-data-jpa)

[Springdoc OpenAPI](https://springdoc.org/)

[Swagger](https://swagger.io/docs/specification/about/)

[Postman](https://www.postman.com/)

[PostgreSQL](https://www.postgresql.org/)

[Docker](https://www.docker.com/)

## Credits
[Iljaas Dhonre](https://github.com/iljaasdhonre)

[Richie Schuurman](https://github.com/RichieSchuurman)

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)
