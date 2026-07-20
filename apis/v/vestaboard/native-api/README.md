# Vestaboard: Native API Reference

A consolidated summary of Vestaboard's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.vestaboard.com/docs/read-write-api/introduction/
- **API base URL:** `https://cloud.vestaboard.com`

## Authentication

### Cloud API Token

Use a Vestaboard Cloud API token from the web or mobile app.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.vestaboard.com/docs/read-write-api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Transition](actions/get-transition.md) | `GET /transition` | [docs](https://docs.vestaboard.com/docs/read-write-api/endpoints/#get-transition) |
| [Read Current Message](actions/read-current-message.md) | `GET /` | [docs](https://docs.vestaboard.com/docs/read-write-api/endpoints/#read-current-message) |
| [Send Message](actions/send-message.md) | `POST /` | [docs](https://docs.vestaboard.com/docs/read-write-api/endpoints/#send-message) |
| [Set Transition](actions/set-transition.md) | `PUT /transition` | [docs](https://docs.vestaboard.com/docs/read-write-api/endpoints/#set-transition) |
