# ScraperAPI: Native API Reference

A consolidated summary of ScraperAPI's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.scraperapi.com
- **API base URL:** `https://api.scraperapi.com`

## Authentication

### API Key

Use a ScraperAPI API key for authenticated requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.scraperapi.com/account-management/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive DataPipeline Project](actions/archive-data-pipeline-project.md) | `DELETE https://datapipeline.scraperapi.com/api/projects/:id` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Cancel Async Job](actions/cancel-async-job.md) | `DELETE https://async.scraperapi.com/jobs/:jobId` | [docs](https://docs.scraperapi.com/asynchronous-api/job-handling) |
| [Cancel DataPipeline Project Job](actions/cancel-data-pipeline-project-job.md) | `DELETE https://datapipeline.scraperapi.com/api/projects/:id/jobs/:jobId` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Amazon Offers DataPipeline Project](actions/create-amazon-offers-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Amazon Product DataPipeline Project](actions/create-amazon-product-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Amazon Reviews DataPipeline Project](actions/create-amazon-reviews-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Amazon Search DataPipeline Project](actions/create-amazon-search-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Async Batch Jobs](actions/create-async-batch-jobs.md) | `POST https://async.scraperapi.com/batchjobs` | [docs](https://docs.scraperapi.com/asynchronous-api/batch-requests) |
| [Create Async Job](actions/create-async-job.md) | `POST https://async.scraperapi.com/jobs` | [docs](https://docs.scraperapi.com/asynchronous-api/job-handling) |
| [Create eBay Product DataPipeline Project](actions/create-ebay-product-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create eBay Search DataPipeline Project](actions/create-ebay-search-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Google Jobs DataPipeline Project](actions/create-google-jobs-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Google News DataPipeline Project](actions/create-google-news-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Google Search DataPipeline Project](actions/create-google-search-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Google Shopping DataPipeline Project](actions/create-google-shopping-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Redfin Agent DataPipeline Project](actions/create-redfin-agent-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Redfin For Rent DataPipeline Project](actions/create-redfin-for-rent-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Redfin For Sale DataPipeline Project](actions/create-redfin-for-sale-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Redfin Search DataPipeline Project](actions/create-redfin-search-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create URL DataPipeline Project](actions/create-url-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/how-to-use) |
| [Create Walmart Category DataPipeline Project](actions/create-walmart-category-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Walmart Product DataPipeline Project](actions/create-walmart-product-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Walmart Review DataPipeline Project](actions/create-walmart-review-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Create Walmart Search DataPipeline Project](actions/create-walmart-search-data-pipeline-project.md) | `POST https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Get Async Job](actions/get-async-job.md) | `GET https://async.scraperapi.com/jobs/:jobId` | [docs](https://docs.scraperapi.com/asynchronous-api/job-handling) |
| [Get DataPipeline Project](actions/get-data-pipeline-project.md) | `GET https://datapipeline.scraperapi.com/api/projects/:id` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [List DataPipeline Project Jobs](actions/list-data-pipeline-project-jobs.md) | `GET https://datapipeline.scraperapi.com/api/projects/:id/jobs` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [List DataPipeline Projects](actions/list-data-pipeline-projects.md) | `GET https://datapipeline.scraperapi.com/api/projects` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
| [Scrape Page](actions/scrape-page.md) | `GET https://api.scraperapi.com` | [docs](https://docs.scraperapi.com/synchronous-apis/using-the-api-endpoint) |
| [Send Scrape Request](actions/send-scrape-request.md) | `POST https://api.scraperapi.com` | [docs](https://docs.scraperapi.com/synchronous-apis/making-post-put-requests) |
| [Update DataPipeline Project](actions/update-data-pipeline-project.md) | `PATCH https://datapipeline.scraperapi.com/api/projects/:id` | [docs](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters) |
