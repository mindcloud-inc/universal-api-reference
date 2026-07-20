# Handwrite: Native API Reference

A consolidated summary of Handwrite's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://documentation.handwrite.io/
- **API base URL:** `https://api.handwrite.io/v1`

## Authentication

### API Key

Use a Handwrite API key from the Handwrite developer dashboard. Handwrite expects the raw key in the Authorization header for every request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://documentation.handwrite.io/)

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
| [Get Order](actions/get-order.md) | `GET /order/:orderId` | [docs](https://documentation.handwrite.io/#get-an-order) |
| [List Handwritings](actions/list-handwritings.md) | `GET /handwriting` | [docs](https://documentation.handwrite.io/#get-handwritings) |
| [List Stationery](actions/list-stationery.md) | `GET /stationery` | [docs](https://documentation.handwrite.io/#get-stationery) |
| [Send Batch Letters](actions/send-batch-letters.md) | `POST /send` | [docs](https://documentation.handwrite.io/#batch-mode) |
| [Send Letter](actions/send-letter.md) | `POST /send` | [docs](https://documentation.handwrite.io/#send-a-letter) |
