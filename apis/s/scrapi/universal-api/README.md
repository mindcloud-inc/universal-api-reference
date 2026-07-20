# <img src="https://images.mindcloud.co/apps/icons/scrapi_1776455840414.png" alt="Scrapi logo" width="28" height="28"> Scrapi: Universal API

Web scraping API with GET/POST scrape endpoints, proxies, browser automation, and callback support.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapi/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrapi.tech
- **Vendor API docs:** https://scrapi.tech/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves the current API credit balance from Scrapi. |

### City

| Action | Method | Description |
| --- | --- | --- |
| [List Country Cities](actions/list-country-cities.md) | GET | Retrieves supported proxy cities for a country from Scrapi. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves supported proxy countries from Scrapi. |

### Scrape Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Scrape Status](actions/get-scrape-status.md) | GET | Retrieves a Scrapi scrape status by callback reference. |
| [Scrape Website](actions/scrape-website.md) | POST | Creates a website scrape job in Scrapi. |

