# Prisma Postgres: Native API Reference

A consolidated summary of Prisma Postgres's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.prisma.io/docs/management-api
- **OpenAPI specification:** https://api.prisma.io/v1/swagger-editor
- **API base URL:** `https://api.prisma.io/v1`

## Authentication

### Prisma Service Token

Authenticate to the Prisma Management API with a Prisma service token sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.prisma.io/docs/management-api/authentication)

## API conventions

Response data is read from `data`. The next-page cursor is read from `pagination.nextCursor`.

## Pagination

Use `limit` in the query string to set the page size. Use `cursor` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Connection](actions/create-connection.md) | `POST /connections` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Create Database](actions/create-database.md) | `POST /databases` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Create Database Connection String](actions/create-database-connection-string.md) | `POST /databases/{databaseId}/connections` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Create Project Database](actions/create-project-database.md) | `POST /projects/{projectId}/databases` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Get Connection](actions/get-connection.md) | `GET /connections/{id}` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Get Database](actions/get-database.md) | `GET /databases/{databaseId}` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Get Database Usage Metrics](actions/get-database-usage-metrics.md) | `GET /databases/{databaseId}/usage` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Get Integration](actions/get-integration.md) | `GET /integrations/{id}` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Get Project](actions/get-project.md) | `GET /projects/{id}` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Database Backups](actions/list-database-backups.md) | `GET /databases/{databaseId}/backups` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Database Connections](actions/list-database-connections.md) | `GET /databases/{databaseId}/connections` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Databases](actions/list-databases.md) | `GET /databases` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Prisma Postgres Regions](actions/list-prisma-postgres-regions.md) | `GET /regions/postgres` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Project Databases](actions/list-project-databases.md) | `GET /projects/{projectId}/databases` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Regions](actions/list-regions.md) | `GET /regions` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Workspace Integrations](actions/list-workspace-integrations.md) | `GET /workspaces/{workspaceId}/integrations` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Rotate Connection Credentials](actions/rotate-connection-credentials.md) | `POST /connections/{id}/rotate` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Update Database](actions/update-database.md) | `PATCH /databases/{databaseId}` | [docs](https://api.prisma.io/v1/swagger-editor) |
| [Update Project](actions/update-project.md) | `PATCH /projects/{id}` | [docs](https://api.prisma.io/v1/swagger-editor) |
