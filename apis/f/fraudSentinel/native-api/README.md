# FraudSentinel: Native API Reference

A consolidated summary of FraudSentinel's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.clickfreeze.io/restapi
- **API base URL:** `https://api.clickfreeze.io`

## Authentication

### API Key

Use the API token from the authenticated ClickFreeze REST API page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.clickfreeze.io/restapi)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get IP Risk](actions/get-ip-risk.md) | `POST /api/sentinel.json` | [docs](https://www.clickfreeze.io/restapi) |
