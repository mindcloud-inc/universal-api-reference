# Perigon: Native API Reference

A consolidated summary of Perigon's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.perigon.io/docs/getting-started
- **API base URL:** `https://api.perigon.io/v1`

## Authentication

### API Key

Authenticate Perigon requests with a Perigon API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.perigon.io/docs/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Journalist By ID](actions/get-journalist-by-id.md) | `GET /v1/journalists/{id}` | [docs](https://docs.perigon.io/docs/journalist-data) |
| [Get Story Counts](actions/get-story-counts.md) | `GET /v1/stories/stats` | [docs](https://docs.perigon.io/docs/stories-overview) |
| [Get Story History](actions/get-story-history.md) | `GET /v1/stories/history` | [docs](https://docs.perigon.io/docs/stories-overview) |
| [Search Articles](actions/search-articles.md) | `GET /v1/articles/all` | [docs](https://docs.perigon.io/docs/overview) |
| [Search Companies](actions/search-companies.md) | `GET /v1/companies/all` | [docs](https://docs.perigon.io/docs/company-data) |
| [Search Journalists](actions/search-journalists.md) | `GET /v1/journalists/all` | [docs](https://docs.perigon.io/docs/journalist-data) |
| [Search People](actions/search-people.md) | `GET /v1/people/all` | [docs](https://docs.perigon.io/docs/entity-search) |
| [Search Sources](actions/search-sources.md) | `GET /v1/sources/all` | [docs](https://docs.perigon.io/docs/sources-source-groups) |
| [Search Stories](actions/search-stories.md) | `GET /v1/stories/all` | [docs](https://docs.perigon.io/docs/stories-overview) |
| [Search Summarizer](actions/search-summarizer.md) | `POST /v1/summarize` | [docs](https://docs.perigon.io/docs/search-summarizer) |
| [Search Topics](actions/search-topics.md) | `GET /v1/topics/all` | [docs](https://docs.perigon.io/docs/topics) |
| [Search Wikipedia](actions/search-wikipedia.md) | `GET /v1/wikipedia/all` | [docs](https://docs.perigon.io/docs/wikipedia) |
| [Vector Search Articles](actions/vector-search-articles.md) | `POST /v1/vector/news/all` | [docs](https://docs.perigon.io/docs/vector-endpoint) |
| [Vector Search Wikipedia](actions/vector-search-wikipedia.md) | `POST /v1/vector/wikipedia/all` | [docs](https://docs.perigon.io/docs/vector-wikipedia) |
