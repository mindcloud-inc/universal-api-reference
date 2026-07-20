# SMMCode: Native API Reference

A consolidated summary of SMMCode's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://extended.smmcode.org/api
- **API base URL:** `https://extended.smmcode.org`

## Authentication

### API Key

Use an SMMCode API key. The API documentation identifies the required credential parameter as `key`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://extended.smmcode.org/api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Order](actions/add-order.md) | `POST /api/v2` | [docs](https://extended.smmcode.org/api) |
| [Get Multiple Order Statuses](actions/get-multiple-order-statuses.md) | `POST /api/v2` | [docs](https://extended.smmcode.org/api) |
| [Get Order Status](actions/get-order-status.md) | `POST /api/v2` | [docs](https://extended.smmcode.org/api) |
| [Get User Balance](actions/get-user-balance.md) | `POST /api/v2` | [docs](https://extended.smmcode.org/api) |
| [List Services](actions/list-services.md) | `POST /api/v2` | [docs](https://extended.smmcode.org/api) |
