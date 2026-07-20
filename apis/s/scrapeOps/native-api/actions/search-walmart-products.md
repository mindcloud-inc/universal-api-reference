# Search Walmart Products with ScrapeOps

Retrieves Walmart search results from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/walmart/search`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Search Walmart Products](https://scrapeops.io/docs/data-api/walmart-product-search-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | The 2-letter country code to scrape Walmart search results from. |
| `query` | query | `string` | no | Walmart search query. |
| `tld` | query | `string` | no | The Walmart top-level domain to scrape, such as com or ca. |
| `url` | query | `string` | no | Full Walmart search URL to fetch. |
