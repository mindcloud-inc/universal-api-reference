# Hasura: Native API Reference

A consolidated summary of Hasura's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://hasura.io/docs/2.0/api-reference/cloud-api-reference/
- **API base URL:** `https://data.pro.hasura.io`

## Authentication

### Personal Access Token

Use a Hasura Cloud Personal Access Token. Requests authenticate with `Authorization: pat {{credentials.apiKey}}`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /v1/graphql` | [docs](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#create-a-project) |
| [Delete Tenant](actions/delete-tenant.md) | `POST /v1/graphql` | [docs](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#delete-a-tenant) |
| [Get Project Tenant ID](actions/get-project-tenant-id.md) | `POST /v1/graphql` | [docs](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#get-project-tenant-id) |
| [Get Tenant Details](actions/get-tenant-details.md) | `POST /v1/graphql` | [docs](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#get-tenant-details) |
| [Get Tenant ENV Vars](actions/get-tenant-env-vars.md) | `POST /v1/graphql` | [docs](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#get-env-vars) |
| [List Projects](actions/list-projects.md) | `POST /v1/graphql` | [docs](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#apis) |
| [Update Tenant ENV Vars](actions/update-tenant-env-vars.md) | `POST /v1/graphql` | [docs](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#update-env-vars) |
