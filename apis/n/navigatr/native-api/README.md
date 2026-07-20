# Navigatr: Native API Reference

A consolidated summary of Navigatr's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://api.navigatr.app/docs
- **OpenAPI specification:** https://api.navigatr.app/openapi.json
- **API base URL:** `https://api.navigatr.app/v1`

## Authentication

### PAT Header Token (Custom)

Use a Navigatr personal access token and send it as X-Access-Token. Do not send this token as an Authorization bearer token.

### Credentials

- **Personal Access Token:** `apiKey` · optional · Your Navigatr personal access token.

Send these headers with each API request:

```http
X-Access-Token: <apiKey>
```

[Official authentication documentation](https://api.navigatr.app/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `size` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get User Detail](actions/get-user-detail.md) | `GET /user_detail/:user_id` | [docs](https://api.navigatr.app/docs#/User%20Detail/user_detail_read_user_detail) |
| [List Badge Assertions](actions/list-badge-assertions.md) | `GET /badge_assertion/` | [docs](https://api.navigatr.app/docs#/Badge%20Assertion/badge_assertion_read_badge_assertions) |
| [List Badges](actions/list-badges.md) | `GET /badge/` | [docs](https://api.navigatr.app/docs#/Badge/badge_read_badges) |
| [List User Badges](actions/list-user-badges.md) | `GET /user_detail/:user_id/badges` | [docs](https://api.navigatr.app/docs#/User%20Detail/user_detail_read_user_badges) |
| [List User Communities](actions/list-user-communities.md) | `GET /user_detail/:user_id/communities` | [docs](https://api.navigatr.app/docs#/User%20Detail/user_detail_read_user_communities) |
