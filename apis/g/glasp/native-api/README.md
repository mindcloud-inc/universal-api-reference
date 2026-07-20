# Glasp: Native API Reference

A consolidated summary of Glasp's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://glasp.co/docs/apis
- **API base URL:** `https://api.glasp.co`

## Authentication

### Access Token

Use a Glasp access token as a bearer token for the Glasp REST API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://glasp.co/docs/apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Highlights](actions/create-highlights.md) | `POST /v1/highlights/create` | [docs](https://glasp.co/docs/apis) |
| [Delete Highlight](actions/delete-highlight.md) | `DELETE /v1/highlights/delete` | [docs](https://glasp.co/docs/apis) |
| [Export Highlights](actions/export-highlights.md) | `GET /v1/highlights/export` | [docs](https://glasp.co/docs/apis) |
| [Update Highlight](actions/update-highlight.md) | `PATCH /v1/highlights/update` | [docs](https://glasp.co/docs/apis) |
