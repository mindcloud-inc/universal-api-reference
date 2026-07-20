# finlight: Native API Reference

A consolidated summary of finlight's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.finlight.me/v2/
- **API base URL:** `https://api.finlight.me`

## Authentication

### API Key

Connect with a Finlight API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.finlight.me/v2/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Article By Link](actions/fetch-article-by-link.md) | `GET /v2/articles/by-link` | [docs](https://docs.finlight.me/v2/rest-endpoints/#fetch-article-by-link) |
| [Fetch Articles](actions/fetch-articles.md) | `POST /v2/articles` | [docs](https://docs.finlight.me/v2/rest-endpoints/#fetch-articles) |
| [List Sources](actions/list-sources.md) | `GET /v2/sources` | [docs](https://docs.finlight.me/v2/rest-endpoints/#get-all-sources) |
