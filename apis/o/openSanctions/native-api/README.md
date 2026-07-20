# OpenSanctions: Native API Reference

A consolidated summary of OpenSanctions's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://api.opensanctions.org/docs
- **OpenAPI specification:** https://api.opensanctions.org/openapi.json
- **API base URL:** `https://api.opensanctions.org`

## Authentication

### API Key

Authenticate hosted OpenSanctions API requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.opensanctions.org/docs/api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (maximum 500). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Health](actions/check-api-health.md) | `GET /healthz` | [docs](https://api.opensanctions.org/docs#/System%20information/healthz_healthz_get) |
| [Check Search Index Readiness](actions/check-search-index-readiness.md) | `GET /readyz` | [docs](https://api.opensanctions.org/docs#/System%20information/readyz_readyz_get) |
| [Get Data Catalog](actions/get-data-catalog.md) | `GET /catalog` | [docs](https://api.opensanctions.org/docs#/Data%20access/catalog_catalog_get) |
| [Get Entity](actions/get-entity.md) | `GET /entities/:entity_id` | [docs](https://api.opensanctions.org/docs#/Data%20access/fetch_entity_entities__entity_id__get) |
| [Get Reconciliation Manifest](actions/get-reconciliation-manifest.md) | `GET /reconcile/:dataset` | [docs](https://api.opensanctions.org/docs#/Reconciliation/reconcile_reconcile__dataset__get) |
| [List Adjacent Entities](actions/list-adjacent-entities.md) | `GET /entities/:entity_id/adjacent` | [docs](https://api.opensanctions.org/docs#/Data%20access/Fetch_Adjacent_Entities__entities__entity_id__adjacent_get) |
| [List Adjacent Entities By Property](actions/list-adjacent-entities-by-property.md) | `GET /entities/:entity_id/adjacent/:property_name` | [docs](https://api.opensanctions.org/docs#/Data%20access/Fetch_Adjacent_by_Property__entities__entity_id__adjacent__property_name__get) |
| [List Entity Statements](actions/list-entity-statements.md) | `GET /statements` | [docs](https://api.opensanctions.org/docs#/Data%20access/statements_statements_get) |
| [List Matching Algorithms](actions/list-matching-algorithms.md) | `GET /algorithms` | [docs](https://api.opensanctions.org/docs#/System%20information/algorithms_algorithms_get) |
| [Match Entity By Example](actions/match-entity-by-example.md) | `POST /match/:dataset` | [docs](https://api.opensanctions.org/docs#/Matching/match_match__dataset__post) |
| [Search Entities](actions/search-entities.md) | `GET /search/:dataset` | [docs](https://api.opensanctions.org/docs#/Matching/search_search__dataset__get) |
