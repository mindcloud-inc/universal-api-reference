# ScrapeGraphAI: Native API Reference

A consolidated summary of ScrapeGraphAI's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.scrapegraphai.com/api-reference/introduction
- **API base URL:** `https://api.scrapegraphai.com/v1`

## Authentication

### API Key

Authenticate ScrapeGraphAI requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
SGAI-APIKEY: <apiKey>
```

[Official authentication documentation](https://docs.scrapegraphai.com/api-reference/endpoint/user/get-credits)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/user/get-credits) |
| [Get Markdownify Status](actions/get-markdownify-status.md) | `GET /markdownify/:request_id` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/markdownify/get-status) |
| [Get SearchScraper Status](actions/get-searchscraper-status.md) | `GET /searchscraper/:request_id` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/searchscraper/get-status) |
| [Get Sitemap Status](actions/get-sitemap-status.md) | `GET /sitemap/:request_id` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/sitemap/get-status) |
| [Get SmartCrawler Status](actions/get-smartcrawler-status.md) | `GET /crawl/:task_id` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/smartcrawler/get-status) |
| [Get SmartScraper Status](actions/get-smartscraper-status.md) | `GET /smartscraper/:request_id` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/smartscraper/get-status) |
| [Start Markdownify](actions/start-markdownify.md) | `POST /markdownify` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/markdownify/start) |
| [Start SearchScraper](actions/start-searchscraper.md) | `POST /searchscraper` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/searchscraper/start) |
| [Start Sitemap](actions/start-sitemap.md) | `POST /sitemap` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/sitemap/start) |
| [Start SmartCrawler](actions/start-smartcrawler.md) | `POST /crawl` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/smartcrawler/start) |
| [Start SmartScraper](actions/start-smartscraper.md) | `POST /smartscraper` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/smartscraper/start) |
| [Submit Feedback](actions/submit-feedback.md) | `POST /feedback` | [docs](https://docs.scrapegraphai.com/api-reference/endpoint/user/submit-feedback) |
