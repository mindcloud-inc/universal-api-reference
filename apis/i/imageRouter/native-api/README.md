# ImageRouter: Native API Reference

A consolidated summary of ImageRouter's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.imagerouter.io/
- **OpenAPI specification:** https://api.imagerouter.io/.well-known/openapi.yaml
- **API base URL:** `https://api.imagerouter.io`

## Authentication

### API Key

Use an ImageRouter API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.imagerouter.io/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100).

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Credit Usage By API Key](actions/get-credit-usage-by-api-key.md) | `GET /v1/credits` | [docs](https://docs.imagerouter.io/api-reference/credits/) |
| [Get Credits](actions/get-credits.md) | `GET /v1/credits` | [docs](https://docs.imagerouter.io/api-reference/credits/) |
| [Get Model](actions/get-model.md) | `GET /v2/models/:modelId` | [docs](https://docs.imagerouter.io/api-reference/models/) |
| [List Models](actions/list-models.md) | `GET /v2/models` | [docs](https://docs.imagerouter.io/api-reference/models/) |
