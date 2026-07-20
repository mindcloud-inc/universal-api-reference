# PeekShot: Native API Reference

A consolidated summary of PeekShot's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.peekshot.com/api-reference
- **API base URL:** `https://api.peekshot.com/api/v1`

## Authentication

### API Key

Authenticate PeekShot requests with the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.peekshot.com/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Screenshot from HTML](actions/create-screenshot-from-html.md) | `POST /html-to-image` | [docs](https://docs.peekshot.com/api-reference/html-to-screenshot-hpie) |
| [Create Screenshot from URL](actions/create-screenshot-from-url.md) | `POST /screenshots` | [docs](https://docs.peekshot.com/api-reference/take-screenshot-ss0c) |
| [Get Screenshot](actions/get-screenshot.md) | `GET /screenshots/:requestId` | [docs](https://docs.peekshot.com/api-reference/get-screenshot-7azv) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.peekshot.com/api-reference/get-projects-list-cbtu) |
| [List Screenshots](actions/list-screenshots.md) | `GET /screenshots` | [docs](https://docs.peekshot.com/api-reference/get-screenshots-list-m4vc) |
