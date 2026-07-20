# Search Amazon products with Scrape do

Finds Amazon products with Scrape do.

## Endpoint

- **Method:** `GET`
- **Path:** `/plugin/amazon/search`
- **Base URL:** `https://api.scrape.do`
- **Official documentation:** [Search Amazon products](https://scrape.do/documentation/amazon-scraper-api/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `geocode` | query | `string` | yes | Amazon marketplace country code such as us, gb, de, or jp. |
| `keyword` | query | `string` | yes | The Amazon search query. |
| `zipcode` | query | `string` | yes | Postal code formatted for the selected marketplace. |
