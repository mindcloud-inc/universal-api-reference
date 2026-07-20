# Get Ebay Store with ScrapeOps

Retrieves eBay store data from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/ebay/store`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Get Ebay Store](https://scrapeops.io/docs/data-api/ebay-store-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `store_name` | query | `string` | no | eBay store name to fetch. |
| `url` | query | `string` | no | Full eBay store URL to fetch. |
