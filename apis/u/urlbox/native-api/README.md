# Urlbox: Native API Reference

A consolidated summary of Urlbox's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://urlbox.com/docs/api
- **API base URL:** `https://api.urlbox.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://urlbox.com/docs/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Render Status](actions/check-render-status.md) | `GET /v1/render/:renderId` | [docs](https://urlbox.com/docs/api#check-the-status-of-a-render) |
| [Create Asynchronous Render](actions/create-asynchronous-render.md) | `POST /v1/render/async` | [docs](https://urlbox.com/docs/api#create-a-render-asynchronously) |
| [Create Synchronous Render](actions/create-synchronous-render.md) | `POST /v1/render/sync` | [docs](https://urlbox.com/docs/api#create-a-render-synchronously) |
