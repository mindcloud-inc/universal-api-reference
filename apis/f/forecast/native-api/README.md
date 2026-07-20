# Forecast: Native API Reference

A consolidated summary of Forecast's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://forecastapi.com/docs/api-reference
- **API base URL:** `https://forecastapi.com/v2`

## Authentication

### API Token

Connect ForecastAPI with a Bearer API token from Team Settings > API Tokens.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://forecastapi.com/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `pageSize` in the query string to set the page size (default 100). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Forecast](actions/generate-forecast.md) | `POST /forecast` | [docs](https://forecastapi.com/docs/api-reference) |
| [Generate Traffic Forecast](actions/generate-traffic-forecast.md) | `POST /traffic-forecasting` | [docs](https://forecastapi.com/docs/api-reference) |
