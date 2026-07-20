# NewsData.io: Native API Reference

A consolidated summary of NewsData.io's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://newsdata.io/documentation
- **API base URL:** `https://newsdata.io/api/1`

## Authentication

### API Key

Use a NewsData.io API key for request authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://newsdata.io/documentation#newsdata-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 10; accepted range 1–50). Use `page` in the query string as the pagination cursor.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Archived News](actions/count-archived-news.md) | `GET /count` | [docs](https://newsdata.io/documentation#count-news) |
| [Count Crypto News](actions/count-crypto-news.md) | `GET /crypto/count` | [docs](https://newsdata.io/documentation#count-news) |
| [Count Market News](actions/count-market-news.md) | `GET /market/count` | [docs](https://newsdata.io/documentation#count-news) |
| [List Archived News](actions/list-archived-news.md) | `GET /archive` | [docs](https://newsdata.io/documentation#news-archive) |
| [List Crypto News](actions/list-crypto-news.md) | `GET /crypto` | [docs](https://newsdata.io/documentation#crypto-news) |
| [List Latest News](actions/list-latest-news.md) | `GET /latest` | [docs](https://newsdata.io/documentation#latest-news) |
| [List Market News](actions/list-market-news.md) | `GET /market` | [docs](https://newsdata.io/documentation#market-news) |
| [List News Sources](actions/list-news-sources.md) | `GET /sources` | [docs](https://newsdata.io/documentation#news-sources) |
