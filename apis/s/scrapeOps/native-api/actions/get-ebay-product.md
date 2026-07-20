# Get Ebay Product with ScrapeOps

Retrieves eBay product data from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/ebay/product`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Get Ebay Product](https://scrapeops.io/docs/data-api/ebay-product-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | query | `string` | no | eBay item ID to fetch. |
| `url` | query | `string` | no | Full eBay product URL to fetch. |
