# Search Amazon with ScrapingDog

Retrieves Amazon search results through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/amazon/search`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Search Amazon](https://docs.scrapingdog.com/amazon-scraper-api/amazon-search-scraper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Target Amazon country code. |
| `domain` | query | `string` | yes | Amazon top-level domain. |
| `page` | query | `string` | no | Amazon search results page. |
| `query` | query | `string` | yes | Amazon search query. |
