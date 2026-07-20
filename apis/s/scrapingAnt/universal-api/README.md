# <img src="https://images.mindcloud.co/apps/icons/scraping-ant_1776875527551.png" alt="ScrapingAnt logo" width="28" height="28"> ScrapingAnt: Universal API

ScrapingAnt is a web scraping API for retrieving web page content through managed browser and proxy infrastructure, with optional rendered HTML, markdown, structured extraction, and API credits usage visibility.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapingAnt/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrapingant.com
- **Vendor API docs:** https://docs.scrapingant.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Credits Usage](actions/get-api-credits-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/get-api-credits-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Api Credits Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get API Credits Usage](actions/get-api-credits-usage.md) | GET | Retrieves subscription status and API credits from ScrapingAnt. |

### Extended Web Page

| Action | Method | Description |
| --- | --- | --- |
| [Scrape URL With Extended JSON](actions/scrape-url-with-extended-json.md) | GET | Retrieves extended JSON page data from ScrapingAnt. |

### Markdown Document

| Action | Method | Description |
| --- | --- | --- |
| [Extract Markdown From URL](actions/extract-markdown-from-url.md) | GET | Retrieves scraped Markdown from a URL in ScrapingAnt. |

### Structured Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Structured Data From URL](actions/extract-structured-data-from-url.md) | GET | Retrieves AI-extracted structured data from a URL in ScrapingAnt. |

### Web Page

| Action | Method | Description |
| --- | --- | --- |
| [Scrape URL](actions/scrape-url.md) | GET | Retrieves scraped page HTML from ScrapingAnt. |
| [Scrape URL With DELETE](actions/scrape-url-with-delete.md) | DELETE | Scrapes a URL with a forwarded DELETE request in ScrapingAnt. |
| [Scrape URL With PATCH](actions/scrape-url-with-patch.md) | PUT |  |
| [Scrape URL With POST](actions/scrape-url-with-post.md) | POST | Scrapes a URL with a forwarded POST request in ScrapingAnt. |
| [Scrape URL With PUT](actions/scrape-url-with-put.md) | PUT | Scrapes a URL with a forwarded PUT request in ScrapingAnt. |

