# DOOMSCROLLR: Native API Reference

A consolidated summary of DOOMSCROLLR's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://doomscrollr.com/api
- **API base URL:** `https://mindcloudapps0402.doomscrollr.com`

## Authentication

### API Key

Use a DOOMSCROLLR API key sent as request field api_key.

### Credentials

- **API Key:** `apiKey` · optional · The DOOMSCROLLR API key from the dashboard API settings.

[Official authentication documentation](https://doomscrollr.com/dashboard/settings#api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 100).

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Audience Member](actions/create-audience-member.md) | `POST /api/audience/create` | [docs](https://doomscrollr.com/api) |
| [Create Content Post](actions/create-content-post.md) | `POST /api/content/posts` | [docs](https://doomscrollr.com/api) |
| [List Audience Members](actions/list-audience-members.md) | `GET /api/audience/list` | [docs](https://doomscrollr.com/api) |
| [List Content Posts](actions/list-content-posts.md) | `GET /api/content/posts` | [docs](https://doomscrollr.com/api) |
| [Verify API Key](actions/verify-api-key.md) | `POST /api/audience/verify` | [docs](https://doomscrollr.com/api) |
