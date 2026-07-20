# lc.cx: Native API Reference

A consolidated summary of lc.cx's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://dev.lc.cx
- **API base URL:** `https://api.lc.cx/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://lc.cx/en/help/how-create-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Short Link](actions/create-short-link.md) | `POST /shorten` | [docs](https://dev.lc.cx) |
| [Create Tags](actions/create-tags.md) | `POST /tags/create` | [docs](https://dev.lc.cx) |
| [Delete Link](actions/delete-link.md) | `DELETE /links/delete/:id` | [docs](https://dev.lc.cx) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/delete/:id` | [docs](https://dev.lc.cx) |
| [Delete Tags in Bulk](actions/delete-tags-in-bulk.md) | `POST /tags/delete/bulk` | [docs](https://dev.lc.cx) |
| [Find Link By Path And Domain](actions/find-link-by-path-and-domain.md) | `GET /links` | [docs](https://dev.lc.cx) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://dev.lc.cx) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:id` | [docs](https://dev.lc.cx) |
| [Get Link](actions/get-link.md) | `GET /links/:id` | [docs](https://dev.lc.cx) |
| [Get Link Click Statistics](actions/get-link-click-statistics.md) | `GET /statistics/links/:id/clicks` | [docs](https://dev.lc.cx) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:id` | [docs](https://dev.lc.cx) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://dev.lc.cx) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://dev.lc.cx) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://dev.lc.cx) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://dev.lc.cx) |
| [Update Link](actions/update-link.md) | `PATCH /links/update/:id` | [docs](https://dev.lc.cx) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/update/:id` | [docs](https://dev.lc.cx) |
| [Update Tags in Bulk](actions/update-tags-in-bulk.md) | `POST /tags/update/bulk` | [docs](https://dev.lc.cx) |
