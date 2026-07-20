# Webcrawler API: Native API Reference

A consolidated summary of Webcrawler API's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://webcrawlerapi.com/docs/getting-started
- **OpenAPI specification:** https://api.webcrawlerapi.com/swagger/doc.json
- **API base URL:** `https://api.webcrawlerapi.com`

## Authentication

### API Key

Authenticate with a WebCrawlerAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://webcrawlerapi.com/docs/access-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 1000; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Crawl Job](actions/cancel-crawl-job.md) | `PUT /v1/job/:id/cancel` | [docs](https://webcrawlerapi.com/docs/api/cancel) |
| [Check Authentication](actions/check-authentication.md) | `GET /v1/auth` | [docs](https://webcrawlerapi.com/docs/access-key) |
| [Create Crawl Job](actions/create-crawl-job.md) | `POST /v1/crawl` | [docs](https://webcrawlerapi.com/docs/api/crawl) |
| [Create Feed](actions/create-feed.md) | `POST /v2/feed` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-create) |
| [Create Scrape Job](actions/create-scrape-job.md) | `POST /v2/scrape` | [docs](https://webcrawlerapi.com/docs/api/scrape) |
| [Delete Feed](actions/delete-feed.md) | `DELETE /v2/feed/:id` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-manage) |
| [Force Run Feed](actions/force-run-feed.md) | `PUT /v2/feed/:id/run` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-manage) |
| [Get Crawl Job](actions/get-crawl-job.md) | `GET /v1/job/:id` | [docs](https://webcrawlerapi.com/docs/api/job) |
| [Get Crawl Job URLs](actions/get-crawl-job-urls.md) | `GET /v1/job/:id/urls` | [docs](https://webcrawlerapi.com/docs/api/urls) |
| [Get Feed](actions/get-feed.md) | `GET /v2/feed/:id` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-get) |
| [Get Feed JSON](actions/get-feed-json.md) | `GET /v2/feed/:id/json` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-json) |
| [Get Feed RSS](actions/get-feed-rss.md) | `GET /v2/feed/:id/rss` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-rss) |
| [Get Organization Usage](actions/get-organization-usage.md) | `GET /v2/organization/usage` | [docs](https://webcrawlerapi.com/docs/api/organization/usage) |
| [Get Scrape Job](actions/get-scrape-job.md) | `GET /v2/scrape/:id` | [docs](https://webcrawlerapi.com/docs/async-requests) |
| [List Feeds](actions/list-feeds.md) | `GET /v2/feeds` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-list) |
| [Pause Feed](actions/pause-feed.md) | `PUT /v2/feed/:id/pause` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-manage) |
| [Ping API](actions/ping-api.md) | `GET /ping` | [docs](https://webcrawlerapi.com/docs/getting-started) |
| [Resend Crawl Job Webhook](actions/resend-crawl-job-webhook.md) | `POST /v1/job/:id/webhook/resend` | [docs](https://webcrawlerapi.com/docs/async-requests) |
| [Resend Feed Webhook](actions/resend-feed-webhook.md) | `POST /v2/feed/:id/webhook/resend` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-manage) |
| [Resume Feed](actions/resume-feed.md) | `PUT /v2/feed/:id/resume` | [docs](https://webcrawlerapi.com/docs/api/feed/feed-manage) |
