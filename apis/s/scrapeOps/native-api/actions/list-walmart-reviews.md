# List Walmart Reviews with ScrapeOps

Retrieves Walmart reviews from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/walmart/review`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [List Walmart Reviews](https://scrapeops.io/docs/data-api/walmart-review-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | — |
| `product_id` | query | `string` | no | Walmart product ID whose reviews to list. |
| `tld` | query | `string` | no | — |
| `url` | query | `string` | no | Full Walmart product URL whose reviews to list. |
