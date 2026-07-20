# Clipcat: Native API Reference

A consolidated summary of Clipcat's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developers.clipcat.com/
- **API base URL:** `https://api.clipcat.com`

## Authentication

### Clipcat API Key

Authenticate Clipcat requests with a workspace API key sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.clipcat.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Render](actions/create-render.md) | `POST /v1/renders` | [docs](https://developers.clipcat.com/) |
| [Get Account](actions/get-account.md) | `GET /v1/account` | [docs](https://developers.clipcat.com/) |
| [Get Authorization Status](actions/get-authorization-status.md) | `GET /v1/auth` | [docs](https://developers.clipcat.com/) |
| [Get Render](actions/get-render.md) | `GET /v1/renders/:uid` | [docs](https://developers.clipcat.com/) |
| [Get Template](actions/get-template.md) | `GET /v1/templates/:uid` | [docs](https://developers.clipcat.com/) |
| [List Renders](actions/list-renders.md) | `GET /v1/renders` | [docs](https://developers.clipcat.com/) |
| [List Templates](actions/list-templates.md) | `GET /v1/templates` | [docs](https://developers.clipcat.com/) |
