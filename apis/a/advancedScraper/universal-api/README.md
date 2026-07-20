# <img src="https://images.mindcloud.co/apps/icons/advanced-scraper_1777654815506.png" alt="Advanced Scraper logo" width="28" height="28"> Advanced Scraper: Universal API

Scrape remote URLs through APILayer Advanced Scraper with rotating IPs, browser rendering, CSS selectors, form submission, and JavaScript execution.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/advancedScraper/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://marketplace.apilayer.com/adv_scraper-api
- **Vendor API docs:** https://marketplace.apilayer.com/adv_scraper-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Scrape URL](actions/scrape-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advancedScraper/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Scraped Page

| Action | Method | Description |
| --- | --- | --- |
| [Scrape URL](actions/scrape-url.md) | GET | Retrieves scraped data from a remote URL in Advanced Scraper. |

