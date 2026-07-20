# AdPage: Native API Reference

A consolidated summary of AdPage's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://whitelabel.adpage.io/api/doc
- **API base URL:** `https://whitelabel.adpage.io`

## Authentication

### API Key

Connect AdPage with an API key from your AdPage account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://whitelabel.adpage.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Agency](actions/get-agency.md) | `GET /api/agency/` | [docs](https://whitelabel.adpage.io/api/doc) |
| [List Section Categories](actions/list-section-categories.md) | `GET /api/section/categories` | [docs](https://whitelabel.adpage.io/api/doc) |
| [Search Agencies](actions/search-agencies.md) | `POST /api/agency/search` | [docs](https://whitelabel.adpage.io/api/doc) |
