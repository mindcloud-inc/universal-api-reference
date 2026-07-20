# ShortPen: Native API Reference

A consolidated summary of ShortPen's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://shortpen.com/docs/api-reference/introduction
- **API base URL:** `https://api.shortpen.com`

## Authentication

### API Key

Connect ShortPen with a workspace-scoped API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://shortpen.com/docs/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Health](actions/check-api-health.md) | `GET /v1/ping` | [docs](https://shortpen.com/docs/api-reference/endpoint/ping) |
| [Create Link](actions/create-link.md) | `POST /v1/generate` | [docs](https://shortpen.com/docs/api-reference/endpoint/generate) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `POST /v1/me` | [docs](https://shortpen.com/docs/api-reference/endpoint/me) |
| [Get Organization](actions/get-organization.md) | `POST /v1/get` | [docs](https://shortpen.com/docs/api-reference/endpoint/get-resources) |
| [List Click Analytics](actions/list-click-analytics.md) | `POST /v1/analytics` | [docs](https://shortpen.com/docs/api-reference/endpoint/analytics) |
| [List Domains](actions/list-domains.md) | `POST /v1/get` | [docs](https://shortpen.com/docs/api-reference/endpoint/get-resources) |
| [List Folders](actions/list-folders.md) | `POST /v1/get` | [docs](https://shortpen.com/docs/api-reference/endpoint/get-resources) |
| [List Link Click Analytics](actions/list-link-click-analytics.md) | `POST /v1/analytics` | [docs](https://shortpen.com/docs/api-reference/endpoint/analytics) |
| [List Links](actions/list-links.md) | `GET /v1/links` | [docs](https://shortpen.com/docs/api-reference/endpoint/list-links) |
| [List Pixels](actions/list-pixels.md) | `POST /v1/get` | [docs](https://shortpen.com/docs/api-reference/endpoint/get-resources) |
| [Update Link](actions/update-link.md) | `PUT /v1/links` | [docs](https://shortpen.com/docs/api-reference/endpoint/edit-link) |
