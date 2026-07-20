# GatewayAPI SMS: Native API Reference

A consolidated summary of GatewayAPI SMS's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://gatewayapi.com/docs/
- **API base URL:** `https://gatewayapi.com`

## Authentication

### API Token

Authenticate with a GatewayAPI API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://gatewayapi.com/docs/authentication/)

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
| [Check Keyword Availability](actions/check-keyword-availability.md) | `POST /api/vas/check` | [docs](https://gatewayapi.com/docs/apis/keywords/) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /rest/me` | [docs](https://gatewayapi.com/docs/apis/prices-balance/) |
| [Get SMS Prices](actions/get-sms-prices.md) | `GET /api/prices/list/sms/:fileformat` | [docs](https://gatewayapi.com/docs/apis/prices-balance/) |
| [Get Usage by Label](actions/get-usage-by-label.md) | `POST /api/usage/labels` | [docs](https://gatewayapi.com/docs/apis/statistics/) |
| [List Keywords](actions/list-keywords.md) | `GET /api/vas` | [docs](https://gatewayapi.com/docs/apis/keywords/) |
