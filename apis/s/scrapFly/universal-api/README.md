# <img src="https://images.mindcloud.co/apps/icons/scrap-fly_1774552406821.png" alt="ScrapFly logo" width="28" height="28"> ScrapFly: Universal API

Scrape pages, capture screenshots, and extract structured web data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapFly/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrapfly.io
- **Vendor API docs:** https://scrapfly.io/docs/openapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Scrape URL](actions/scrape-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fweb-scraping.dev%2Fproduct%2F1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Capture Screenshot](actions/capture-screenshot.md) | GET | Retrieves a webpage screenshot from ScrapFly. |
| [Download Screenshot](actions/download-screenshot.md) | GET | Retrieves a screenshot attachment from ScrapFly. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Batch Crawl Contents](actions/batch-crawl-contents.md) | GET | Retrieves batched crawl contents from ScrapFly. |
| [Extract With Model](actions/extract-with-model.md) | GET | Retrieves extracted data from ScrapFly using AI extraction. |
| [Extract With Prompt](actions/extract-with-prompt.md) | GET | Retrieves extracted data from ScrapFly using an LLM prompt. |
| [Extract With Template](actions/extract-with-template.md) | GET | Retrieves extracted data from ScrapFly using a template. |
| [Get Crawl Contents](actions/get-crawl-contents.md) | GET | Retrieves crawl contents from ScrapFly. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download Crawl Artifact](actions/download-crawl-artifact.md) | GET | Retrieves a crawl artifact from ScrapFly. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Crawl](actions/cancel-crawl.md) | DELETE | Cancels an existing crawl job in ScrapFly. |
| [Get Crawl Status](actions/get-crawl-status.md) | GET | Retrieves crawl job status from ScrapFly. |
| [Start Crawl](actions/start-crawl.md) | POST | Creates a new crawl job in ScrapFly. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [List Crawled URLs](actions/list-crawled-ur-ls.md) | GET | Retrieves crawled URLs from ScrapFly. |
| [Scrape URL](actions/scrape-url.md) | GET | Retrieves a scraped page from ScrapFly. |
| [Scrape URL via PATCH](actions/scrape-url-via-patch.md) | PUT | Updates an existing page scrape in ScrapFly. |
| [Scrape URL via POST](actions/scrape-url-via-post.md) | POST | Creates a new page scrape in ScrapFly. |
| [Scrape URL via PUT](actions/scrape-url-via-put.md) | PUT | Updates an existing page scrape in ScrapFly. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Monitoring Metrics](actions/get-monitoring-metrics.md) | GET | Retrieves monitoring metrics from ScrapFly. |
| [Get Target Metrics](actions/get-target-metrics.md) | GET | Retrieves target monitoring metrics from ScrapFly. |

