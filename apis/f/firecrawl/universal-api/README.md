# <img src="https://images.mindcloud.co/apps/icons/firecrawl_1773692705572.png" alt="Firecrawl logo" width="28" height="28"> Firecrawl: Universal API

Extract, crawl, search, and map web content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/firecrawl/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://firecrawl.dev
- **Vendor API docs:** https://docs.firecrawl.dev/api-reference/v2-introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Scrape URL](actions/scrape-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agent Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Agent](actions/cancel-agent.md) | DELETE | Cancels an agent job in Firecrawl. |
| [Get Agent Status](actions/get-agent-status.md) | GET | Retrieves agent job status from Firecrawl. |
| [Start Agent](actions/start-agent.md) | POST | Creates an agent job in Firecrawl. |

### Batch Scrape Job

| Action | Method | Description |
| --- | --- | --- |
| [Batch Scrape URLs](actions/batch-scrape-urls.md) | POST | Creates a batch scrape job in Firecrawl. |
| [Cancel Batch Scrape](actions/cancel-batch-scrape.md) | DELETE | Cancels a batch scrape job in Firecrawl. |
| [Get Batch Scrape Errors](actions/get-batch-scrape-errors.md) | GET | Retrieves batch scrape errors from Firecrawl. |
| [Get Batch Scrape Status](actions/get-batch-scrape-status.md) | GET | Retrieves batch scrape job status from Firecrawl. |

### Browser Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Browser Session](actions/create-browser-session.md) | POST | Creates a browser session in Firecrawl. |
| [Delete Browser Session](actions/delete-browser-session.md) | DELETE | Deletes a browser session from Firecrawl. |
| [Execute Browser Code](actions/execute-browser-code.md) | PUT | Executes code in a Firecrawl browser session. |
| [List Browser Sessions](actions/list-browser-sessions.md) | GET | Retrieves browser sessions from Firecrawl. |

### Crawl Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Crawl](actions/cancel-crawl.md) | DELETE | Cancels a crawl job in Firecrawl. |
| [Get Active Crawls](actions/get-active-crawls.md) | GET | Retrieves active crawls from Firecrawl. |
| [Get Crawl Errors](actions/get-crawl-errors.md) | GET | Retrieves crawl errors from Firecrawl. |
| [Get Crawl Status](actions/get-crawl-status.md) | GET | Retrieves crawl job status from Firecrawl. |
| [Start Crawl](actions/start-crawl.md) | POST | Creates a crawl job in Firecrawl. |

### Extract Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data](actions/extract-data.md) | POST | Creates a data extraction job in Firecrawl. |
| [Get Extract Status](actions/get-extract-status.md) | GET | Retrieves extraction job status from Firecrawl. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Scrape URL](actions/scrape-url.md) | GET | Scrapes a single URL with Firecrawl. |

### Queue Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Queue Status](actions/get-queue-status.md) | GET | Retrieves queue status from Firecrawl. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Web](actions/search-web.md) | GET | Finds web results with Firecrawl. |

### Team Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Usage](actions/get-credit-usage.md) | GET | Retrieves credit usage from Firecrawl. |
| [Get Token Usage](actions/get-token-usage.md) | GET | Retrieves token usage from Firecrawl. |

### Url Map

| Action | Method | Description |
| --- | --- | --- |
| [Map Website](actions/map-website.md) | GET | Retrieves website URLs from Firecrawl. |

