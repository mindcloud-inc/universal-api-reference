# Get Amazon Product with ScrapingDog

Retrieves Amazon product details through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/amazon/product`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Get Amazon Product](https://docs.scrapingdog.com/amazon-scraper-api/amazon-product-scraper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asin` | query | `string` | yes | Amazon product identifier. |
| `country` | query | `string` | no | Target Amazon country code. |
| `domain` | query | `string` | yes | Amazon top-level domain. |
