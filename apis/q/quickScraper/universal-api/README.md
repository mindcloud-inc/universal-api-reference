# <img src="https://images.mindcloud.co/apps/icons/d296c317-d9d6-4cf4-b39f-1cf463aa3b33-2_1775056639226.png" alt="Quick Scraper logo" width="28" height="28"> Quick Scraper: Universal API

Extract webpage HTML and parser-backed data through Quick Scraper's proxy-backed scraping API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quickScraper/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quickscraper.co/
- **Vendor API docs:** https://quickscraper.co/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Parse URL](actions/parse-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/parse-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account details from Quick Scraper. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Parse URL](actions/parse-url.md) | GET | Retrieves scraped page content from Quick Scraper. |

