# ScrapeOps: Native API Reference

A consolidated summary of ScrapeOps's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://scrapeops.io/docs/intro/
- **API base URL:** `http://headers.scrapeops.io/v1`

## Authentication

### API Key

Connect with your ScrapeOps API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://scrapeops.io/docs/n8n/setup/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Browse Walmart Products](actions/browse-walmart-products.md) | `GET https://proxy.scrapeops.io/v1/structured-data/walmart/browse` | [docs](https://scrapeops.io/docs/data-api/walmart-browse-api/) |
| [Create Scheduled Job](actions/create-scheduled-job.md) | `POST https://backend.scrapeops.io/v1/client/scheduled-jobs` | [docs](https://scrapeops.io/docs/servers-scheduling/rest-api/) |
| [Delete Scheduled Job](actions/delete-scheduled-job.md) | `DELETE https://backend.scrapeops.io/v1/client/scheduled-jobs/:jobId` | [docs](https://scrapeops.io/docs/servers-scheduling/rest-api/) |
| [Fetch And Parse Url With Custom Parser](actions/fetch-and-parse-url-with-custom-parser.md) | `GET https://proxy.scrapeops.io/v1/` | [docs](https://scrapeops.io/docs/parser-api/custom-parser/) |
| [Fetch Url Via Proxy Api Aggregator](actions/fetch-url-via-proxy-api-aggregator.md) | `GET https://proxy.scrapeops.io/v1/` | [docs](https://scrapeops.io/docs/web-scraping-proxy-api-aggregator/quickstart/) |
| [Get Amazon Product](actions/get-amazon-product.md) | `GET https://proxy.scrapeops.io/v1/structured-data/amazon/product` | [docs](https://scrapeops.io/docs/data-api/amazon-product-api/) |
| [Get Ebay Product](actions/get-ebay-product.md) | `GET https://proxy.scrapeops.io/v1/structured-data/ebay/product` | [docs](https://scrapeops.io/docs/data-api/ebay-product-api/) |
| [Get Ebay Store](actions/get-ebay-store.md) | `GET https://proxy.scrapeops.io/v1/structured-data/ebay/store` | [docs](https://scrapeops.io/docs/data-api/ebay-store-api/) |
| [Get Indeed Job](actions/get-indeed-job.md) | `GET https://proxy.scrapeops.io/v1/structured-data/indeed/job-detail` | [docs](https://scrapeops.io/docs/data-api/indeed-job-detail-api/) |
| [Get Walmart Product](actions/get-walmart-product.md) | `GET https://proxy.scrapeops.io/v1/structured-data/walmart/product` | [docs](https://scrapeops.io/docs/data-api/walmart-product-api/) |
| [List All Scheduled Jobs](actions/list-all-scheduled-jobs.md) | `GET https://backend.scrapeops.io/v1/client/scheduled-jobs` | [docs](https://scrapeops.io/docs/servers-scheduling/rest-api/) |
| [List Browser Headers](actions/list-browser-headers.md) | `GET /browser-headers` | [docs](https://scrapeops.io/docs/fake-user-agent-headers-api/fake-browser-headers/) |
| [List Ebay Categories](actions/list-ebay-categories.md) | `GET https://proxy.scrapeops.io/v1/structured-data/ebay/category` | [docs](https://scrapeops.io/docs/data-api/ebay-category-api/) |
| [List Ebay Feedback](actions/list-ebay-feedback.md) | `GET https://proxy.scrapeops.io/v1/structured-data/ebay/feedback` | [docs](https://scrapeops.io/docs/data-api/ebay-feedback-api/) |
| [List Fake User Agents](actions/list-fake-user-agents.md) | `GET http://headers.scrapeops.io/v1/user-agents` | [docs](https://scrapeops.io/docs/fake-user-agent-headers-api/fake-user-agents/) |
| [List Servers](actions/list-servers.md) | `GET https://backend.scrapeops.io/v1/client/servers` | [docs](https://scrapeops.io/docs/servers-scheduling/rest-api/) |
| [List Spiders By Server Id](actions/list-spiders-by-server-id.md) | `GET https://backend.scrapeops.io/v1/client/servers/:serverId/spiders` | [docs](https://scrapeops.io/docs/servers-scheduling/rest-api/) |
| [List Walmart Categories](actions/list-walmart-categories.md) | `GET https://proxy.scrapeops.io/v1/structured-data/walmart/category` | [docs](https://scrapeops.io/docs/data-api/walmart-category-api/) |
| [List Walmart Reviews](actions/list-walmart-reviews.md) | `GET https://proxy.scrapeops.io/v1/structured-data/walmart/review` | [docs](https://scrapeops.io/docs/data-api/walmart-review-api/) |
| [List Walmart Shop Results](actions/list-walmart-shop-results.md) | `GET https://proxy.scrapeops.io/v1/structured-data/walmart/shop` | [docs](https://scrapeops.io/docs/data-api/walmart-shop-api/) |
| [Parse Html With Custom Parser](actions/parse-html-with-custom-parser.md) | `POST https://parser.scrapeops.io/v1/custom-parser` | [docs](https://scrapeops.io/docs/parser-api/custom-parser/) |
| [Run Spider](actions/run-spider.md) | `POST https://backend.scrapeops.io/v1/client/spiders/run` | [docs](https://scrapeops.io/docs/servers-scheduling/rest-api/) |
| [Search Amazon Products](actions/search-amazon-products.md) | `GET https://proxy.scrapeops.io/v1/structured-data/amazon/search` | [docs](https://scrapeops.io/docs/data-api/amazon-product-search-api/) |
| [Search Ebay Listings](actions/search-ebay-listings.md) | `GET https://proxy.scrapeops.io/v1/structured-data/ebay/search` | [docs](https://scrapeops.io/docs/data-api/ebay-search-api/) |
| [Search Indeed Companies](actions/search-indeed-companies.md) | `GET https://proxy.scrapeops.io/v1/structured-data/indeed/company-search` | [docs](https://scrapeops.io/docs/data-api/indeed-company-search-api/) |
| [Search Indeed Jobs](actions/search-indeed-jobs.md) | `GET https://proxy.scrapeops.io/v1/structured-data/indeed/job-search` | [docs](https://scrapeops.io/docs/data-api/indeed-job-search-api/) |
| [Search Walmart Products](actions/search-walmart-products.md) | `GET https://proxy.scrapeops.io/v1/structured-data/walmart/search` | [docs](https://scrapeops.io/docs/data-api/walmart-product-search-api/) |
