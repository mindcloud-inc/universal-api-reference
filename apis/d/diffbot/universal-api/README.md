# <img src="https://images.mindcloud.co/apps/icons/diffbot-icon_1782393189452.png" alt="Diffbot logo" width="28" height="28"> Diffbot: Universal API

Diffbot extracts structured web content, queries the Knowledge Graph, enriches person and organization records, and manages crawl and bulk extraction jobs through the official Diffbot APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/diffbot/latest
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.diffbot.com/
- **Vendor API docs:** https://docs.diffbot.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves Diffbot account details and usage information. |

### Analyzed Page

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Page](actions/analyze-page.md) | GET | Analyzes a page and classifies its content with Diffbot. |

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Extract Article](actions/extract-article.md) | GET | Extracts article content from a page with Diffbot. |

### Bulk Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Extract Job](actions/get-bulk-extract-job.md) | GET | Retrieves details for a Diffbot bulk extract job. |
| [List Bulk Extract Jobs](actions/list-bulk-extract-jobs.md) | GET | Lists bulk extract jobs in Diffbot. |

### Bulk Job Data

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Bulk Extract Job Data](actions/retrieve-bulk-extract-job-data.md) | GET | Downloads extracted data for a Diffbot bulk extract job. |

### Collection Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Crawl Or Bulk Job](actions/search-crawl-or-bulk-job.md) | GET | Searches a Diffbot crawl or bulk job with DQL. |

### Combined Entity

| Action | Method | Description |
| --- | --- | --- |
| [Combine Enhancements](actions/combine-enhancements.md) | GET | Enriches a person and current employer in Diffbot. |

### Coverage Report

| Action | Method | Description |
| --- | --- | --- |
| [Get DQL Coverage Report By ID](actions/get-dql-coverage-report-by-id.md) | GET | Retrieves a DQL coverage report from Diffbot by ID. |
| [Get DQL Coverage Report By Query](actions/get-dql-coverage-report-by-query.md) | GET | Retrieves a DQL coverage report from Diffbot by query. |

### Crawl Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Crawl Job](actions/get-crawl-job.md) | GET | Retrieves details for a Diffbot crawl job. |
| [List Crawl Jobs](actions/list-crawl-jobs.md) | GET | Lists available crawl jobs in Diffbot. |

### Crawl Job Data

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Crawl Job Data](actions/retrieve-crawl-job-data.md) | GET | Downloads extracted data for a Diffbot crawl job. |

### Custom Api

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Custom APIs](actions/retrieve-custom-apis.md) | GET | Retrieves Custom APIs defined on the current Diffbot token. |

### Custom Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract With Custom API](actions/extract-with-custom-api.md) | GET | Extracts a page with a named Diffbot Custom API. |

### Discussion

| Action | Method | Description |
| --- | --- | --- |
| [Extract Discussion](actions/extract-discussion.md) | GET | Extracts discussion threads from a page with Diffbot. |

### Enhance Bulk Item

| Action | Method | Description |
| --- | --- | --- |
| [Download Enhance Bulkjob Result](actions/download-enhance-bulkjob-result.md) | GET | Downloads a single result from a Diffbot Enhance bulk job. |

### Enhance Bulk Result

| Action | Method | Description |
| --- | --- | --- |
| [Download Enhance Bulkjob Results](actions/download-enhance-bulkjob-results.md) | GET | Downloads results for a completed Diffbot Enhance bulk job. |
| [Download Enhance Bulkjob Results (POST)](actions/download-enhance-bulkjob-results-post.md) | GET | Downloads results for a completed Diffbot Enhance bulk job using POST. |

### Enhance Bulkjob

| Action | Method | Description |
| --- | --- | --- |
| [List Enhance Bulkjobs](actions/list-enhance-bulkjobs.md) | GET | Lists Enhance bulk jobs for the current Diffbot token. |
| [Poll Enhance Bulkjob Status](actions/poll-enhance-bulkjob-status.md) | GET | Retrieves the status of a Diffbot Enhance bulk job. |

### Enhance Coverage Report

| Action | Method | Description |
| --- | --- | --- |
| [Download Enhance Bulkjob Coverage Report](actions/download-enhance-bulkjob-coverage-report.md) | GET | Downloads the coverage report for a Diffbot Enhance bulk job. |

### Enhanced Entity

| Action | Method | Description |
| --- | --- | --- |
| [Enhance Entity](actions/enhance-entity.md) | GET | Enhances a person or organization record in Diffbot. |
| [Enhance Entity (POST)](actions/enhance-entity-post.md) | GET | Enhances a person or organization record in Diffbot using POST. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Extract Event](actions/extract-event.md) | GET | Extracts event details from a page with Diffbot. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Extract Image](actions/extract-image.md) | GET | Extracts primary image details from a page with Diffbot. |

### Job Posting

| Action | Method | Description |
| --- | --- | --- |
| [Extract Job](actions/extract-job.md) | GET | Extracts job posting details from a page with Diffbot. |

### Knowledge Graph Query

| Action | Method | Description |
| --- | --- | --- |
| [Search With DQL](actions/search-with-dql.md) | GET | Searches the Diffbot Knowledge Graph with a DQL query. |
| [Search With DQL (POST)](actions/search-with-dql-post.md) | GET | Searches the Diffbot Knowledge Graph with DQL using POST. |

### Language Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Process Text](actions/process-text.md) | GET | Processes raw text with Diffbot Natural Language API. |

### List Page

| Action | Method | Description |
| --- | --- | --- |
| [Extract List](actions/extract-list.md) | GET | Extracts a structured item list from a page with Diffbot. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Extract Product](actions/extract-product.md) | GET | Extracts product details from a page with Diffbot. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Extract Video](actions/extract-video.md) | GET | Extracts video details from a page with Diffbot. |

