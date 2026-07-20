# Scrape do: Native API Reference

A consolidated summary of Scrape do's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://scrape.do/documentation/
- **API base URL:** `https://api.scrape.do`

## Authentication

### API key

Use your Scrape.do API token for sync and async endpoints.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://scrape.do/documentation/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel async job](actions/cancel-async-job.md) | `DELETE https://q.scrape.do/api/v1/jobs/:jobID` | [docs](https://scrape.do/documentation/async-api/cancel-job/) |
| [Create async scraping job](actions/create-async-scraping-job.md) | `POST https://q.scrape.do/api/v1/jobs` | [docs](https://scrape.do/documentation/async-api/create-job/) |
| [Fetch webpage](actions/fetch-webpage.md) | `GET /` | [docs](https://scrape.do/documentation/) |
| [Get Amazon offers](actions/get-amazon-offers.md) | `GET /plugin/amazon/offer-listing` | [docs](https://scrape.do/documentation/amazon-scraper-api/offer-listing/) |
| [Get Amazon product details](actions/get-amazon-product-details.md) | `GET /plugin/amazon/pdp` | [docs](https://scrape.do/documentation/amazon-scraper-api/pdp/) |
| [Get Amazon raw HTML](actions/get-amazon-raw-html.md) | `GET /plugin/amazon/` | [docs](https://scrape.do/documentation/amazon-scraper-api/raw-html/) |
| [Get async job details](actions/get-async-job-details.md) | `GET https://q.scrape.do/api/v1/jobs/:jobID` | [docs](https://scrape.do/documentation/async-api/get-job/) |
| [Get async task details](actions/get-async-task-details.md) | `GET https://q.scrape.do/api/v1/jobs/:jobID/:taskID` | [docs](https://scrape.do/documentation/async-api/get-task/) |
| [Get async user info](actions/get-async-user-info.md) | `GET https://q.scrape.do/api/v1/me` | [docs](https://scrape.do/documentation/async-api/get-me/) |
| [Get Google trending now](actions/get-google-trending-now.md) | `GET /plugin/google/trending` | [docs](https://scrape.do/documentation/google-trends-api/trending/) |
| [Get Google trends data](actions/get-google-trends-data.md) | `GET /plugin/google/trends` | [docs](https://scrape.do/documentation/google-trends-api/trends/) |
| [Get usage statistics](actions/get-usage-statistics.md) | `GET /info` | [docs](https://scrape.do/documentation/api-response/usage-stats) |
| [List async jobs](actions/list-async-jobs.md) | `GET https://q.scrape.do/api/v1/jobs` | [docs](https://scrape.do/documentation/async-api/list-jobs/) |
| [Search Amazon products](actions/search-amazon-products.md) | `GET /plugin/amazon/search` | [docs](https://scrape.do/documentation/amazon-scraper-api/search/) |
| [Search Google](actions/search-google.md) | `GET /plugin/google/search` | [docs](https://scrape.do/documentation/google-search-api/) |
| [Send DELETE request](actions/send-delete-request.md) | `DELETE /` | [docs](https://scrape.do/documentation/api-response/post-put-request/) |
| [Send PATCH request](actions/send-patch-request.md) | `PATCH /` | [docs](https://scrape.do/documentation/api-response/post-put-request/) |
| [Send POST request](actions/send-post-request.md) | `POST /` | [docs](https://scrape.do/documentation/api-response/post-put-request/) |
| [Send PUT request](actions/send-put-request.md) | `PUT /` | [docs](https://scrape.do/documentation/api-response/post-put-request/) |
| [Use Google AI mode](actions/use-google-ai-mode.md) | `GET /plugin/google/search/ai-mode` | [docs](https://scrape.do/documentation/google-search-api/ai-mode/) |
