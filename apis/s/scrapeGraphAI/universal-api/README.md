# <img src="https://images.mindcloud.co/apps/icons/scrape-graph-ai_1774377874842.png" alt="ScrapeGraphAI logo" width="28" height="28"> ScrapeGraphAI: Universal API

Scrape websites and extract structured data with AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapeGraphAI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrapegraphai.com
- **Vendor API docs:** https://docs.scrapegraphai.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Crawltask

| Action | Method | Description |
| --- | --- | --- |
| [Get SmartCrawler Status](actions/get-smartcrawler-status.md) | GET | Retrieves SmartCrawler task status from ScrapeGraphAI. |
| [Start SmartCrawler](actions/start-smartcrawler.md) | POST | Starts a SmartCrawler crawl job in ScrapeGraphAI. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves current credit balance from ScrapeGraphAI. |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Submit Feedback](actions/submit-feedback.md) | POST | Submits rating feedback for a ScrapeGraphAI request. |

### Markdownifyrequest

| Action | Method | Description |
| --- | --- | --- |
| [Get Markdownify Status](actions/get-markdownify-status.md) | GET | Retrieves Markdownify request status from ScrapeGraphAI. |
| [Start Markdownify](actions/start-markdownify.md) | POST | Starts a Markdownify conversion job in ScrapeGraphAI. |

### Searchscraperrequest

| Action | Method | Description |
| --- | --- | --- |
| [Get SearchScraper Status](actions/get-searchscraper-status.md) | GET | Retrieves SearchScraper request status from ScrapeGraphAI. |
| [Start SearchScraper](actions/start-searchscraper.md) | POST | Starts a SearchScraper search job in ScrapeGraphAI. |

### Sitemaprequest

| Action | Method | Description |
| --- | --- | --- |
| [Get Sitemap Status](actions/get-sitemap-status.md) | GET | Retrieves sitemap request status from ScrapeGraphAI. |
| [Start Sitemap](actions/start-sitemap.md) | POST | Starts a sitemap extraction job in ScrapeGraphAI. |

### Smartscraperrequest

| Action | Method | Description |
| --- | --- | --- |
| [Get SmartScraper Status](actions/get-smartscraper-status.md) | GET | Retrieves SmartScraper request status from ScrapeGraphAI. |
| [Start SmartScraper](actions/start-smartscraper.md) | POST | Starts a SmartScraper extraction job in ScrapeGraphAI. |

