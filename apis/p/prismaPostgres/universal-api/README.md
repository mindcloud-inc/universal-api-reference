# <img src="https://images.mindcloud.co/apps/icons/prisma-hd_1776291094437.png" alt="Prisma Postgres logo" width="28" height="28"> Prisma Postgres: Universal API

Manage Prisma Postgres workspaces, projects, databases, connections, integrations, backups, and usage through the Prisma Management API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/prismaPostgres/latest
- **Category:** IT Operations / Database
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.prisma.io/postgres
- **Vendor API docs:** https://www.prisma.io/docs/management-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Create Connection](actions/create-connection.md) | POST | Creates a new connection in Prisma Postgres. |
| [Create Database Connection String](actions/create-database-connection-string.md) | POST | Creates a database connection string in Prisma Postgres. |
| [Get Connection](actions/get-connection.md) | GET | Retrieves a connection from Prisma Postgres. |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from Prisma Postgres. |
| [List Database Connections](actions/list-database-connections.md) | GET | Retrieves database connections from Prisma Postgres. |
| [Rotate Connection Credentials](actions/rotate-connection-credentials.md) | PUT | Rotates credentials for a Prisma Postgres connection. |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a new database in Prisma Postgres. |
| [Create Project Database](actions/create-project-database.md) | POST | Creates a new project database in Prisma Postgres. |
| [Get Database](actions/get-database.md) | GET | Retrieves a database from Prisma Postgres. |
| [List Databases](actions/list-databases.md) | GET | Retrieves databases from Prisma Postgres. |
| [List Project Databases](actions/list-project-databases.md) | GET | Retrieves project databases from Prisma Postgres. |
| [Update Database](actions/update-database.md) | PUT | Updates an existing database in Prisma Postgres. |

### Database Backup

| Action | Method | Description |
| --- | --- | --- |
| [List Database Backups](actions/list-database-backups.md) | GET | Retrieves database backups from Prisma Postgres. |

### Database Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Usage Metrics](actions/get-database-usage-metrics.md) | GET | Retrieves database usage metrics from Prisma Postgres. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration](actions/get-integration.md) | GET | Retrieves an integration from Prisma Postgres. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from Prisma Postgres. |
| [List Workspace Integrations](actions/list-workspace-integrations.md) | GET | Retrieves workspace integrations from Prisma Postgres. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Prisma Postgres. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Prisma Postgres. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Prisma Postgres. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Prisma Postgres. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [List Prisma Postgres Regions](actions/list-prisma-postgres-regions.md) | GET | Retrieves Prisma Postgres regions. |
| [List Regions](actions/list-regions.md) | GET | Retrieves regions from Prisma Postgres. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Prisma Postgres. |

