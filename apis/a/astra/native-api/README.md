# Astra: Native API Reference

A consolidated summary of Astra's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.datastax.com/en/astra-api-docs/_attachments/devops-api/index.html
- **API base URL:** `https://api.astra.datastax.com`

## Authentication

### Application Token

Use a DataStax Astra application token (AstraCS:...) to authenticate DevOps API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.datastax.com/en/astra-db-classic/administration/manage-application-tokens.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | `POST /v2/databases` |  |
| [Get Current Org](actions/get-current-org.md) | `GET /v2/currentOrg` | [docs](https://docs.datastax.com/en/astra-api-docs/_attachments/devops-api/index.html#tag/Organization-Operations/operation/getCurrentOrg) |
| [Get Database](actions/get-database.md) | `GET /v2/databases/:databaseId` |  |
| [Get Datacenter Private Link](actions/get-datacenter-private-link.md) | `GET /v2/organizations/clusters/:databaseId/datacenters/:datacenterId/private-link` |  |
| [Get Organization User](actions/get-organization-user.md) | `GET /v2/organizations/users/:userId` |  |
| [List Available Regions](actions/list-available-regions.md) | `GET /v2/regions/serverless` |  |
| [List Database Datacenters](actions/list-database-datacenters.md) | `GET /v2/databases/:databaseId/datacenters` |  |
| [List Databases](actions/list-databases.md) | `GET /v2/databases` |  |
| [List Organization Private Links](actions/list-organization-private-links.md) | `GET /v2/organizations/private-link` |  |
| [List Organization Users](actions/list-organization-users.md) | `GET /v2/organizations/users` |  |
