# NTD Web Calculator API

Spring Boot 4 REST API for the NTD arithmetic calculator. It provides JWT authentication, transactional balance debits, operation history, soft deletion, and Random.org integration.

## Requirements

- JDK 21
- Gradle wrapper
- MySQL 8.4 for deployment-like local runs, or H2 for lightweight local development/tests

## Run locally

```powershell
.\gradlew.bat bootRun
```

The API runs at `http://localhost:8090` and uses an H2 file database under `data/` by default.

## Tests

```powershell
.\gradlew.bat test
```

## Configuration

Configuration is read from environment variables:

- `SERVER_PORT`
- `DB_URL`, `DB_USERNAME`, `DB_PASSWORD`, `DB_DRIVER`
- `JPA_DDL_AUTO`
- `JWT_SECRET`
- `CORS_ALLOWED_ORIGINS`
- `H2_CONSOLE_ENABLED`

Use a deployment-grade `JWT_SECRET` outside local development.

## API

See [`docs/API.md`](docs/API.md) for the versioned REST contract and [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) for service guarantees.
