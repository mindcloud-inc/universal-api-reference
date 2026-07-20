# ScrapFly: Native API Reference

A consolidated summary of ScrapFly's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://scrapfly.io/docs/openapi
- **API base URL:** `https://api.scrapfly.io`

## Authentication

### API Key

Use a ScrapFly project API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://scrapfly.io/docs/project)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Crawl Contents](actions/batch-crawl-contents.md) | `POST /crawl/:crawlerUuid/contents/batch` | [docs](https://scrapfly.io/docs/crawler-api/results) |
| [Cancel Crawl](actions/cancel-crawl.md) | `DELETE /crawl/:crawlerUuid` | [docs](https://scrapfly.io/docs/crawler-api/faq) |
| [Capture Screenshot](actions/capture-screenshot.md) | `GET /screenshot` | [docs](https://scrapfly.io/docs/screenshot-api/getting-started) |
| [Download Crawl Artifact](actions/download-crawl-artifact.md) | `GET /crawl/:crawlerUuid/artifact` | [docs](https://scrapfly.io/docs/crawler-api/results) |
| [Download Screenshot](actions/download-screenshot.md) | `GET /screenshot/:screenshotId/main` | [docs](https://scrapfly.io/docs/screenshot-api/getting-started) |
| [Extract With Model](actions/extract-with-model.md) | `POST /extraction` | [docs](https://scrapfly.io/docs/extraction-api/automatic-ai) |
| [Extract With Prompt](actions/extract-with-prompt.md) | `POST /extraction` | [docs](https://scrapfly.io/docs/extraction-api/llm-prompt) |
| [Extract With Template](actions/extract-with-template.md) | `POST /extraction` | [docs](https://scrapfly.io/docs/extraction-api/rules-and-template) |
| [Get Crawl Contents](actions/get-crawl-contents.md) | `GET /crawl/:crawlerUuid/contents` | [docs](https://scrapfly.io/docs/crawler-api/results) |
| [Get Crawl Status](actions/get-crawl-status.md) | `GET /crawl/:crawlerUuid/status` | [docs](https://scrapfly.io/docs/crawler-api/getting-started) |
| [Get Monitoring Metrics](actions/get-monitoring-metrics.md) | `GET /scrape/monitoring/metrics` | [docs](https://scrapfly.io/docs/monitoring) |
| [Get Target Metrics](actions/get-target-metrics.md) | `GET /scrape/monitoring/metrics/target` | [docs](https://scrapfly.io/docs/monitoring) |
| [List Crawled URLs](actions/list-crawled-ur-ls.md) | `GET /crawl/:crawlerUuid/urls` | [docs](https://scrapfly.io/docs/crawler-api/results) |
| [Scrape URL](actions/scrape-url.md) | `GET /scrape` | [docs](https://scrapfly.io/docs/scrape-api/getting-started) |
| [Scrape URL via PATCH](actions/scrape-url-via-patch.md) | `PATCH /scrape` | [docs](https://scrapfly.io/docs/scrape-api/getting-started) |
| [Scrape URL via POST](actions/scrape-url-via-post.md) | `POST /scrape` | [docs](https://scrapfly.io/docs/scrape-api/getting-started) |
| [Scrape URL via PUT](actions/scrape-url-via-put.md) | `PUT /scrape` | [docs](https://scrapfly.io/docs/scrape-api/getting-started) |
| [Start Crawl](actions/start-crawl.md) | `POST /crawl` | [docs](https://scrapfly.io/docs/crawler-api/getting-started) |
