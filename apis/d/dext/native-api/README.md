# Dext: Native API Reference

A consolidated summary of Dext's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://help.dext.com/en/articles/272702-data-health-insights-api
- **API base URL:** `https://api.precision.dext.com`

## Authentication

### API Key

Connect with a Dext API bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.dext.com/en/articles/272702-data-health-insights-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Client](actions/get-client.md) | `GET /clients/:client_id` | [docs](https://help.dext.com/en/articles/272702-data-health-insights-api) |
| [Get Client Activity Stats](actions/get-client-activity-stats.md) | `GET /clients/:client_id/activity-stats` | [docs](https://help.dext.com/en/articles/272702-data-health-insights-api) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://help.dext.com/en/articles/272702-data-health-insights-api) |
