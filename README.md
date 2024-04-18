A simple CRUD api using Spring and Spring data JPA. And implementing JWT auth with Spring Security
<br>
1. Start the application with Maven
2. The API will be accessible at http://localhost:8080


## API Endpoints
The API provides the following endpoints:

```markdown

POST /auth/login - Login into the App

POST /auth/register - Register a new user into the App

GET /product - Retrieve a list of all data.

POST /product - Register a new data.

PUT /product - Alter data.

DELETE /product/{id} - Inactivate data.

```
## Authentication
The API uses Spring Security for authentication control. The following roles are available:

```
USER -> Standard user role for logged-in users.
ADMIN -> Admin role for managing partners (registering new partners).
```
To access protected endpoints as an ADMIN user, provide the appropriate authentication credentials in the request header.
## Database
The project uses PostgresSQL as the database. The necessary database migrations are managed using Flyway.
