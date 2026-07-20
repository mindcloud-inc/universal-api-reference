# <img src="https://images.mindcloud.co/apps/icons/scrapeunblocker-icon_1775751236322.png" alt="ScrapeUnblocker logo" width="28" height="28"> ScrapeUnblocker: Universal API

Fetch webpage HTML and proxied image content through ScrapeUnblocker's RapidAPI-backed scraping service.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapeUnblocker/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.scrapeunblocker.com
- **Vendor API docs:** https://www.scrapeunblocker.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Page Source](actions/get-page-source.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeUnblocker/latest/actions/get-page-source?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Source](actions/get-page-source.md) | GET | Retrieves page source from ScrapeUnblocker. |

