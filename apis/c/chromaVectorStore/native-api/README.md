# Chroma Vector Store: Native API Reference

A consolidated summary of Chroma Vector Store's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.trychroma.com/reference/chroma-api
- **API base URL:** `https://api.trychroma.com`

## Authentication

### API Key

Authenticate to Chroma Cloud with an x-chroma-token API key and tenant UUID.

### Credentials

- **API Key:** `apiKey` · required
- **Tenant ID:** `tenant` · required · Chroma tenant UUID required for tenant-scoped collection, database, and record endpoints.

Send these headers with each API request:

```http
x-chroma-token: <apiKey>
```

[Official authentication documentation](https://docs.trychroma.com/reference/chroma-api/authentication/get-user-identity)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database` | path | `string` | yes | Chroma database name, also surfaced in the product as a workspace ID. |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/create-collection) |
| [Create Database](actions/create-database.md) | `POST /api/v2/tenants/:tenant/databases` | [docs](https://docs.trychroma.com/reference/chroma-api/database/create-database) |
| [Create Tenant](actions/create-tenant.md) | `POST /api/v2/tenants` | [docs](https://docs.trychroma.com/reference/chroma-api/tenant/create-tenant) |
| [Fork Collection](actions/fork-collection.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/fork` | [docs](https://docs.trychroma.com/api-reference/collection/fork-collection) |
| [Get Records](actions/get-records.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/get` | [docs](https://docs.trychroma.com/reference/chroma-api/record/get-records) |
| [Get User Identity](actions/get-user-identity.md) | `GET /api/v2/auth/identity` | [docs](https://docs.trychroma.com/reference/chroma-api/authentication/get-user-identity) |
| [Heartbeat](actions/heartbeat.md) | `GET /api/v2/heartbeat` | [docs](https://docs.trychroma.com/reference/chroma-api/system/heartbeat) |
| [List Databases](actions/list-databases.md) | `GET /api/v2/tenants/:tenant/databases` | [docs](https://docs.trychroma.com/reference/chroma-api/database/list-databases) |
| [List Sources](actions/list-sources.md) | `GET https://sync.trychroma.com/api/v1/sources` | [docs](https://docs.trychroma.com/reference/sync-api/source/list-sources) |
