# companydata.dk: Native API Reference

A consolidated summary of companydata.dk's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.companydata.dk/v1/docs
- **OpenAPI specification:** https://api.companydata.dk/v1/openapi.json
- **API base URL:** `https://api.companydata.dk`

## Authentication

### API Key

Authenticate to the companydata.dk API with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://companydata.dk/en/guider/api-adgang)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pagination.pages`. The current page number is read from `pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /v1/account` | [docs](https://api.companydata.dk/v1/docs#tag/Account/operation/get_account_v1_account_get) |
