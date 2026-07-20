# Dappier: Native API Reference

A consolidated summary of Dappier's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.dappier.com/api-reference
- **API base URL:** `https://api.dappier.com`

## Authentication

### API Key

Use a Dappier API key as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dappier.com/real-time-data-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `num_results` in the request body to set the page size (default 10). Use `page` in the request body to choose the page; numbering starts at 1.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get AI Recommendations By Query](actions/get-ai-recommendations-by-query.md) | `POST /app/v2/search` | [docs](https://docs.dappier.com/api-reference/endpoint/ai-recommendations) |
| [Get Cat Care Recommendations](actions/get-cat-care-recommendations.md) | `POST /app/v2/search` | [docs](https://docs.dappier.com/api-reference/endpoint/ai-recommendations) |
| [Get Domain-Constrained Recommendations](actions/get-domain-constrained-recommendations.md) | `POST /app/v2/search` | [docs](https://docs.dappier.com/api-reference/endpoint/ai-recommendations) |
| [Get Most Recent Recommendations](actions/get-most-recent-recommendations.md) | `POST /app/v2/search` | [docs](https://docs.dappier.com/api-reference/endpoint/ai-recommendations) |
| [Get Trending Recommendations](actions/get-trending-recommendations.md) | `POST /app/v2/search` | [docs](https://docs.dappier.com/api-reference/endpoint/ai-recommendations) |
| [Search Real Time Data](actions/search-real-time-data.md) | `POST /app/aimodel/:aiModelId` | [docs](https://docs.dappier.com/api-reference/endpoint/real-time-search) |
