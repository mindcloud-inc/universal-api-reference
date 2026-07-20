# Chroma Cloud: Native API Reference

A consolidated summary of Chroma Cloud's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.trychroma.com/cloud/getting-started
- **OpenAPI specification:** https://api.trychroma.com:8000/openapi.json
- **API base URL:** `https://api.trychroma.com`

## Authentication

### API Key

Connect Chroma Cloud with an API key sent in the x-chroma-token header.

### Credentials

- **API Key:** `apiKey` · required
- **Tenant ID:** `tenant` · required · Chroma Cloud tenant ID. Used as the `{tenant}` path parameter for tenant-scoped Core API actions.
- **Database Name:** `database` · required · Chroma Cloud database name. The Chroma client docs also allow this through CHROMA_DATABASE.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.trychroma.com/reference/chroma-api/authentication/get-user-identity)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 0). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add records](actions/add-records.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/add` | [docs](https://docs.trychroma.com/reference/chroma-api/record/add-records) |
| [Attach function](actions/attach-function.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/functions/attach` | [docs](https://docs.trychroma.com/api-reference/function/attach-function) |
| [Cancel invocation](actions/cancel-invocation.md) | `PUT https://sync.trychroma.com/api/v1/invocations/:invocation_id` | [docs](https://docs.trychroma.com/reference/sync-api/invocation/cancel-invocation) |
| [Create collection](actions/create-collection.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/create-collection) |
| [Create database](actions/create-database.md) | `POST /api/v2/tenants/:tenant/databases` | [docs](https://docs.trychroma.com/reference/chroma-api/database/create-database) |
| [Create invocation](actions/create-invocation.md) | `POST https://sync.trychroma.com/api/v1/sources/:source_id/invocations` | [docs](https://docs.trychroma.com/reference/sync-api/invocation/create-invocation) |
| [Create source](actions/create-source.md) | `POST https://sync.trychroma.com/api/v1/sources` | [docs](https://docs.trychroma.com/reference/sync-api/source/create-source) |
| [Create tenant](actions/create-tenant.md) | `POST /api/v2/tenants` | [docs](https://docs.trychroma.com/reference/chroma-api/tenant/create-tenant) |
| [Delete collection](actions/delete-collection.md) | `DELETE /api/v2/tenants/:tenant/databases/:database/collections/:collection_id` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/delete-collection) |
| [Delete database](actions/delete-database.md) | `DELETE /api/v2/tenants/:tenant/databases/:database` | [docs](https://docs.trychroma.com/reference/chroma-api/database/delete-database) |
| [Delete records](actions/delete-records.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/delete` | [docs](https://docs.trychroma.com/reference/chroma-api/record/delete-records) |
| [Delete source](actions/delete-source.md) | `DELETE https://sync.trychroma.com/api/v1/sources/:source_id` | [docs](https://docs.trychroma.com/reference/sync-api/source/delete-source) |
| [Detach function](actions/detach-function.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/attached_functions/:name/detach` | [docs](https://docs.trychroma.com/api-reference/function/detach-function) |
| [Fork collection](actions/fork-collection.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/fork` | [docs](https://docs.trychroma.com/api-reference/collection/fork-collection) |
| [Get attached function](actions/get-attached-function.md) | `GET /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/functions/:function_name` | [docs](https://docs.trychroma.com/api-reference/function/get-attached-function) |
| [Get collection](actions/get-collection.md) | `GET /api/v2/tenants/:tenant/databases/:database/collections/:collection_id` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/get-collection) |
| [Get collection by ID](actions/get-collection-by-id.md) | `GET /api/v2/tenants/:tenant/databases/:database/collections/by-id/:collection_id` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/get-collection-by-id) |
| [Get database](actions/get-database.md) | `GET /api/v2/tenants/:tenant/databases/:database` | [docs](https://docs.trychroma.com/reference/chroma-api/database/get-database) |
| [Get fork count](actions/get-fork-count.md) | `GET /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/fork_count` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/get-fork-count) |
| [Get indexing status](actions/get-indexing-status.md) | `GET /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/indexing_status` | [docs](https://docs.trychroma.com/reference/chroma-api/record/get-indexing-status) |
| [Get invocation](actions/get-invocation.md) | `GET https://sync.trychroma.com/api/v1/invocations/:invocation_id` | [docs](https://docs.trychroma.com/reference/sync-api/invocation/get-invocation) |
| [Get latest invocations by keys](actions/get-latest-invocations-by-keys.md) | `POST https://sync.trychroma.com/api/v1/sources/:source_id/invocations/latest-by-keys` | [docs](https://docs.trychroma.com/reference/sync-api/invocation/get-latest-invocations-by-keys) |
| [Get number of collections](actions/get-number-of-collections.md) | `GET /api/v2/tenants/:tenant/databases/:database/collections_count` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/get-number-of-collections) |
| [Get number of records](actions/get-number-of-records.md) | `GET /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/count` | [docs](https://docs.trychroma.com/reference/chroma-api/record/get-number-of-records) |
| [Get records](actions/get-records.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/get` | [docs](https://docs.trychroma.com/reference/chroma-api/record/get-records) |
| [Get source](actions/get-source.md) | `GET https://sync.trychroma.com/api/v1/sources/:source_id` | [docs](https://docs.trychroma.com/reference/sync-api/source/get-source) |
| [Get tenant](actions/get-tenant.md) | `GET /api/v2/tenants/:tenant` | [docs](https://docs.trychroma.com/reference/chroma-api/tenant/get-tenant) |
| [Get user identity](actions/get-user-identity.md) | `GET /api/v2/auth/identity` | [docs](https://docs.trychroma.com/reference/chroma-api/authentication/get-user-identity) |
| [Get version](actions/get-version.md) | `GET /api/v2/version` | [docs](https://docs.trychroma.com/reference/chroma-api/system/get-version) |
| [List collections](actions/list-collections.md) | `GET /api/v2/tenants/:tenant/databases/:database/collections` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/list-collections) |
| [List databases](actions/list-databases.md) | `GET /api/v2/tenants/:tenant/databases` | [docs](https://docs.trychroma.com/reference/chroma-api/database/list-databases) |
| [List invocations](actions/list-invocations.md) | `GET https://sync.trychroma.com/api/v1/invocations` | [docs](https://docs.trychroma.com/reference/sync-api/invocation/list-invocations) |
| [List sources](actions/list-sources.md) | `GET https://sync.trychroma.com/api/v1/sources` | [docs](https://docs.trychroma.com/reference/sync-api/source/list-sources) |
| [Pre-flight checks](actions/pre-flight-checks.md) | `GET /api/v2/pre-flight-checks` | [docs](https://docs.trychroma.com/reference/chroma-api/system/pre-flight-checks) |
| [Query collection](actions/query-collection.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/query` | [docs](https://docs.trychroma.com/reference/chroma-api/record/query-collection) |
| [Search records](actions/search-records.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/search` | [docs](https://docs.trychroma.com/reference/chroma-api/record/search-records) |
| [Update collection](actions/update-collection.md) | `PUT /api/v2/tenants/:tenant/databases/:database/collections/:collection_id` | [docs](https://docs.trychroma.com/reference/chroma-api/collection/update-collection) |
| [Update records](actions/update-records.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/update` | [docs](https://docs.trychroma.com/reference/chroma-api/record/update-records) |
| [Update tenant](actions/update-tenant.md) | `PATCH /api/v2/tenants/:tenant` | [docs](https://docs.trychroma.com/reference/chroma-api/tenant/update-tenant) |
| [Upsert records](actions/upsert-records.md) | `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/upsert` | [docs](https://docs.trychroma.com/reference/chroma-api/record/upsert-records) |
