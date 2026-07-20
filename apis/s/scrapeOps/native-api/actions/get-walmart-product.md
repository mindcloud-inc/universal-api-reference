# Get Walmart Product with ScrapeOps

Retrieves Walmart product data from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/walmart/product`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Get Walmart Product](https://scrapeops.io/docs/data-api/walmart-product-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | The 2-letter country code to scrape Walmart product data from. |
| `product_id` | query | `string` | no | Walmart product ID to fetch. |
| `tld` | query | `string` | no | — |
| `url` | query | `string` | no | Full Walmart product URL to fetch. |
