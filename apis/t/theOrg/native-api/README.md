# The Org: Native API Reference

A consolidated summary of The Org's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://developers.theorg.com/api
- **API base URL:** `https://api.theorg.com`

## Authentication

### API Key

Use your The Org API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://developers.theorg.com/api/get-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Estimate Position Search Credit Usage](actions/estimate-position-search-credit-usage.md) | `POST /v1.1/positions/credit-usage` | [docs](https://developers.theorg.com/api/endpoints/position-api) |
| [Find Manager](actions/find-manager.md) | `GET /v1.1/companies/org-chart/managers` | [docs](https://developers.theorg.com/api/endpoints/company-api) |
| [Find Positions](actions/find-positions.md) | `POST /v1.1/positions` | [docs](https://developers.theorg.com/api/endpoints/position-api) |
| [Get Current Usage](actions/get-current-usage.md) | `GET /v1.1/usage` | [docs](https://developers.theorg.com/api/endpoints/usage-api) |
| [Get Historical Usage](actions/get-historical-usage.md) | `GET /v1.1/usage/history` | [docs](https://developers.theorg.com/api/endpoints/usage-api) |
