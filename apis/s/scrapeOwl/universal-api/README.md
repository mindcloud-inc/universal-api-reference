# <img src="https://images.mindcloud.co/apps/icons/scrape-owl_1776783191513.png" alt="ScrapeOwl logo" width="28" height="28"> ScrapeOwl: Universal API

ScrapeOwl is a web scraping and data extraction API for fetching pages, extracting elements, rendering JavaScript, using proxies, and checking account usage.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapeOwl/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrapeowl.com
- **Vendor API docs:** https://scrapeowl.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOwl/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Scraped Page

| Action | Method | Description |
| --- | --- | --- |
| [Scrape URL](actions/scrape-url.md) | GET |  |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET |  |

