# User API

Spring Boot REST API with CRUD endpoints for the `User` entity, backed by PostgreSQL + JPA/Hibernate.

## Prerequisites

- Java 17+
- Maven 3.9+
- PostgreSQL running locally (or update `src/main/resources/application.yml`)

## Database setup

```sql
CREATE DATABASE userdb;
```

Update credentials in `src/main/resources/application.yml` if needed.

## Run

```bash
mvn spring-boot:run
```

## Test

```bash
mvn test
```

Tests use an in-memory H2 database (`src/test/resources/application.yml`), so PostgreSQL is not required to run the test suite.

## Endpoints

| Method | Path              | Description        |
|--------|-------------------|---------------------|
| POST   | /api/users        | Create a user       |
| GET    | /api/users        | List all users      |
| GET    | /api/users/{id}   | Get user by id      |
| PUT    | /api/users/{id}   | Update user by id   |
| DELETE | /api/users/{id}   | Delete user by id   |

### Sample request body

```json
{
  "name": "Jane Doe",
  "email": "jane.doe@example.com"
}
```
