# DotSimple: Native API Reference

A consolidated summary of DotSimple's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.dotsimple.io/en/collections/8-api-referenz
- **API base URL:** `https://app.dotsimple.io/app/api`

## Authentication

### API Key

Use a DotSimple access token for API requests.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace UUID:** `workspaceUuid` · required · The DotSimple workspace UUID used in API paths.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.dotsimple.io/en/articles/64-create-access-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | `GET /:workspaceUuid/accounts` | [docs](https://help.dotsimple.io/en/articles/65-accounts) |
