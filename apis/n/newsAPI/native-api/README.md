# News API: Native API Reference

A consolidated summary of News API's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://newsapi.org/docs
- **API base URL:** `https://newsapi.org/v2`

## Authentication

### API Key

Connect a News API account with an API key sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://newsapi.org/docs/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | `GET /top-headlines/sources` | [docs](https://newsapi.org/docs/endpoints/sources) |
| [List Top Headlines](actions/list-top-headlines.md) | `GET /top-headlines` | [docs](https://newsapi.org/docs/endpoints/top-headlines) |
| [Search Everything](actions/search-everything.md) | `GET /everything` | [docs](https://newsapi.org/docs/endpoints/everything) |
