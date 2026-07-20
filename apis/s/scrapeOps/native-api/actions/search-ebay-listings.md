# Search Ebay Listings with ScrapeOps

Retrieves eBay search results from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/ebay/search`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Search Ebay Listings](https://scrapeops.io/docs/data-api/ebay-search-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | eBay search query. |
| `url` | query | `string` | no | Full eBay search URL to fetch. |
