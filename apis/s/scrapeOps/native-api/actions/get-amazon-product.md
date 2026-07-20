# Get Amazon Product with ScrapeOps

Retrieves Amazon product data from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/amazon/product`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Get Amazon Product](https://scrapeops.io/docs/data-api/amazon-product-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asin` | query | `string` | no | Amazon ASIN for the product to fetch. |
| `url` | query | `string` | no | Full Amazon product URL to fetch. |
