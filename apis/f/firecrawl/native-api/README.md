# Firecrawl: Native API Reference

A consolidated summary of Firecrawl's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.firecrawl.dev/api-reference/v2-introduction
- **OpenAPI specification:** https://docs.firecrawl.dev/api-reference/v2-openapi.json
- **API base URL:** `https://api.firecrawl.dev/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.firecrawl.dev/api-reference/v2-introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Scrape URLs](actions/batch-scrape-urls.md) | `POST /batch/scrape` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/batch-scrape) |
| [Cancel Agent](actions/cancel-agent.md) | `DELETE /agent/:jobId` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/agent-delete) |
| [Cancel Batch Scrape](actions/cancel-batch-scrape.md) | `DELETE /batch/scrape/:id` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/batch-scrape-delete) |
| [Cancel Crawl](actions/cancel-crawl.md) | `DELETE /crawl/:id` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/crawl-delete) |
| [Create Browser Session](actions/create-browser-session.md) | `POST /browser` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/browser-create) |
| [Delete Browser Session](actions/delete-browser-session.md) | `DELETE /browser/:sessionId` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/browser-delete) |
| [Execute Browser Code](actions/execute-browser-code.md) | `POST /browser/:sessionId/execute` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/browser-execute) |
| [Extract Data](actions/extract-data.md) | `POST /extract` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/extract) |
| [Get Active Crawls](actions/get-active-crawls.md) | `GET /crawl/active` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/crawl-active) |
| [Get Agent Status](actions/get-agent-status.md) | `GET /agent/:jobId` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/agent-get) |
| [Get Batch Scrape Errors](actions/get-batch-scrape-errors.md) | `GET /batch/scrape/:id/errors` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/batch-scrape-get-errors) |
| [Get Batch Scrape Status](actions/get-batch-scrape-status.md) | `GET /batch/scrape/:id` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/batch-scrape-get) |
| [Get Crawl Errors](actions/get-crawl-errors.md) | `GET /crawl/:id/errors` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/crawl-get-errors) |
| [Get Crawl Status](actions/get-crawl-status.md) | `GET /crawl/:id` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/crawl-get) |
| [Get Credit Usage](actions/get-credit-usage.md) | `GET /team/credit-usage` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/credit-usage) |
| [Get Extract Status](actions/get-extract-status.md) | `GET /extract/:id` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/extract-get) |
| [Get Queue Status](actions/get-queue-status.md) | `GET /team/queue-status` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/queue-status) |
| [Get Token Usage](actions/get-token-usage.md) | `GET /team/token-usage` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/token-usage) |
| [List Browser Sessions](actions/list-browser-sessions.md) | `GET /browser` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/browser-list) |
| [Map Website](actions/map-website.md) | `POST /map` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/map) |
| [Scrape URL](actions/scrape-url.md) | `POST /scrape` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/scrape) |
| [Search Web](actions/search-web.md) | `POST /search` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/search) |
| [Start Agent](actions/start-agent.md) | `POST /agent` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/agent) |
| [Start Crawl](actions/start-crawl.md) | `POST /crawl` | [docs](https://docs.firecrawl.dev/api-reference/endpoint/crawl-post) |
