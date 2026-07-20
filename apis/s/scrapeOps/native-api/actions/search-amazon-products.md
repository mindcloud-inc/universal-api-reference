# Search Amazon Products with ScrapeOps

Retrieves Amazon search results from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/amazon/search`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Search Amazon Products](https://scrapeops.io/docs/data-api/amazon-product-search-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Amazon search query. |
| `url` | query | `string` | no | Full Amazon search URL to fetch. |
