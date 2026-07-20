# List Amazon Reviews with ScrapingDog

Retrieves Amazon product reviews through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/amazon/reviews`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [List Amazon Reviews](https://docs.scrapingdog.com/amazon-scraper-api/amazon-reviews-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asin` | query | `string` | yes | Amazon product identifier. |
| `domain` | query | `string` | yes | Amazon top-level domain. |
| `page` | query | `string` | yes | Amazon reviews page. |
