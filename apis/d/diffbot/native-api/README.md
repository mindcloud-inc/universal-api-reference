# Diffbot: Native API Reference

A consolidated summary of Diffbot's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://docs.diffbot.com/reference
- **OpenAPI specification:** https://kg.diffbot.com/kg/dql/openapi.json
- **API base URL:** `https://api.diffbot.com`

## Authentication

### API Token

Use your Diffbot token. Diffbot requires the token as the documented query parameter `token` rather than a bearer header.

### Credentials

- **API Token:** `apiKey` · required · Your Diffbot API token. MindCloud stores this token once and sends it as the documented query parameter `token` on every request.

[Official authentication documentation](https://docs.diffbot.com/reference/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Page](actions/analyze-page.md) | `GET /v3/analyze` | [docs](https://docs.diffbot.com/reference/analyze) |
| [Combine Enhancements](actions/combine-enhancements.md) | `GET https://kg.diffbot.com/kg/v3/enhance/combine` | [docs](https://docs.diffbot.com/reference/combine) |
| [Download Enhance Bulkjob Coverage Report](actions/download-enhance-bulkjob-coverage-report.md) | `GET https://kg.diffbot.com/kg/v3/enhance/bulk/report/{bulkjobId}/{reportId}` | [docs](https://docs.diffbot.com/reference/download-bulkjob-coverage-report) |
| [Download Enhance Bulkjob Result](actions/download-enhance-bulkjob-result.md) | `GET https://kg.diffbot.com/kg/v3/enhance/bulk/{bulkjobId}/{jobIdx}` | [docs](https://docs.diffbot.com/reference/download-single-result-of-bulkjob) |
| [Download Enhance Bulkjob Results](actions/download-enhance-bulkjob-results.md) | `GET https://kg.diffbot.com/kg/v3/enhance/bulk/{bulkjobId}` | [docs](https://docs.diffbot.com/reference/download-results-of-bulkjob) |
| [Download Enhance Bulkjob Results (POST)](actions/download-enhance-bulkjob-results-post.md) | `POST https://kg.diffbot.com/kg/v3/enhance/bulk/{bulkjobId}` | [docs](https://docs.diffbot.com/reference/download-results-of-bulkjob) |
| [Enhance Entity](actions/enhance-entity.md) | `GET https://kg.diffbot.com/kg/v3/enhance` | [docs](https://docs.diffbot.com/reference/enhance) |
| [Enhance Entity (POST)](actions/enhance-entity-post.md) | `POST https://kg.diffbot.com/kg/v3/enhance` | [docs](https://docs.diffbot.com/reference/enhance) |
| [Extract Article](actions/extract-article.md) | `GET /v3/article` | [docs](https://docs.diffbot.com/reference/article) |
| [Extract Discussion](actions/extract-discussion.md) | `GET /v3/discussion` | [docs](https://docs.diffbot.com/reference/discussion) |
| [Extract Event](actions/extract-event.md) | `GET /v3/event` | [docs](https://docs.diffbot.com/reference/event) |
| [Extract Image](actions/extract-image.md) | `GET /v3/image` | [docs](https://docs.diffbot.com/reference/image) |
| [Extract Job](actions/extract-job.md) | `GET /v3/job` | [docs](https://docs.diffbot.com/reference/job) |
| [Extract List](actions/extract-list.md) | `GET /v3/list` | [docs](https://docs.diffbot.com/reference/list) |
| [Extract Product](actions/extract-product.md) | `GET /v3/product` | [docs](https://docs.diffbot.com/reference/product) |
| [Extract Video](actions/extract-video.md) | `GET /v3/video` | [docs](https://docs.diffbot.com/reference/video) |
| [Extract With Custom API](actions/extract-with-custom-api.md) | `GET /v3/custom` | [docs](https://docs.diffbot.com/reference/custom) |
| [Get Account](actions/get-account.md) | `GET /v4/account` | [docs](https://docs.diffbot.com/reference/account) |
| [Get Bulk Extract Job](actions/get-bulk-extract-job.md) | `GET /v3/bulk/` | [docs](https://docs.diffbot.com/reference/manage-a-bulk-extract-job) |
| [Get Crawl Job](actions/get-crawl-job.md) | `GET /v3/crawl` | [docs](https://docs.diffbot.com/reference/manage-a-crawl-job) |
| [Get DQL Coverage Report By ID](actions/get-dql-coverage-report-by-id.md) | `GET https://kg.diffbot.com/kg/v3/dql/report/{id}` | [docs](https://docs.diffbot.com/reference/reportget) |
| [Get DQL Coverage Report By Query](actions/get-dql-coverage-report-by-query.md) | `GET https://kg.diffbot.com/kg/v3/dql/report` | [docs](https://docs.diffbot.com/reference/reportfind) |
| [List Bulk Extract Jobs](actions/list-bulk-extract-jobs.md) | `GET /v3/bulk/` | [docs](https://docs.diffbot.com/reference/manage-a-bulk-extract-job) |
| [List Crawl Jobs](actions/list-crawl-jobs.md) | `GET /v3/crawl` | [docs](https://docs.diffbot.com/reference/list-all-crawl-jobs) |
| [List Enhance Bulkjobs](actions/list-enhance-bulkjobs.md) | `GET https://kg.diffbot.com/kg/v3/enhance/bulk/status` | [docs](https://docs.diffbot.com/reference/list-bulkjobs-for-token) |
| [Poll Enhance Bulkjob Status](actions/poll-enhance-bulkjob-status.md) | `GET https://kg.diffbot.com/kg/v3/enhance/bulk/{bulkjobId}/status` | [docs](https://docs.diffbot.com/reference/poll-bulkjob-status) |
| [Process Text](actions/process-text.md) | `POST https://nl.diffbot.com/v1/` | [docs](https://docs.diffbot.com/reference/process-text) |
| [Retrieve Bulk Extract Job Data](actions/retrieve-bulk-extract-job-data.md) | `GET /v3/bulk/data` | [docs](https://docs.diffbot.com/reference/retrieve-bulk-extract-job-data) |
| [Retrieve Crawl Job Data](actions/retrieve-crawl-job-data.md) | `GET /v3/crawl/data` | [docs](https://docs.diffbot.com/reference/retrieve-crawl-job-data) |
| [Retrieve Custom APIs](actions/retrieve-custom-apis.md) | `GET /v3/custom` | [docs](https://docs.diffbot.com/reference/retrieve-custom-apis) |
| [Search Crawl Or Bulk Job](actions/search-crawl-or-bulk-job.md) | `GET /v3/search/` | [docs](https://docs.diffbot.com/reference/search-a-crawlbulk-job) |
| [Search With DQL](actions/search-with-dql.md) | `GET https://kg.diffbot.com/kg/v3/dql` | [docs](https://docs.diffbot.com/reference/search-with-dql) |
| [Search With DQL (POST)](actions/search-with-dql-post.md) | `POST https://kg.diffbot.com/kg/v3/dql` | [docs](https://docs.diffbot.com/reference/search-with-dql) |
