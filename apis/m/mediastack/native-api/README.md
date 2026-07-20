# Mediastack: Native API Reference

A consolidated summary of Mediastack's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://mediastack.com/documentation
- **API base URL:** `https://api.mediastack.com/v1`

## Authentication

### API Key

Authenticate Mediastack requests with the account API access key sent as the access_key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mediastack.com/documentation)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Use `published_asc` for ascending order and `published_desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Search Historical News](actions/search-historical-news.md) | `GET /news` | [docs](https://mediastack.com/documentation) |
| [Search News](actions/search-news.md) | `GET /news` | [docs](https://mediastack.com/documentation) |
| [Search News Sources](actions/search-news-sources.md) | `GET /sources` | [docs](https://mediastack.com/documentation) |
