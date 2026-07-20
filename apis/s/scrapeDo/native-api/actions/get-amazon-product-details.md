# Get Amazon product details with Scrape do

Retrieves Amazon product details with Scrape do.

## Endpoint

- **Method:** `GET`
- **Path:** `/plugin/amazon/pdp`
- **Base URL:** `https://api.scrape.do`
- **Official documentation:** [Get Amazon product details](https://scrape.do/documentation/amazon-scraper-api/pdp/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asin` | query | `string` | yes | The 10-character Amazon product identifier. |
| `geocode` | query | `string` | yes | Amazon marketplace country code such as us, gb, de, or jp. |
| `zipcode` | query | `string` | yes | Postal code formatted for the selected marketplace. |
