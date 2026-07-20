# Get Amazon raw HTML with Scrape do

Retrieves Amazon raw HTML with Scrape do.

## Endpoint

- **Method:** `GET`
- **Path:** `/plugin/amazon/`
- **Base URL:** `https://api.scrape.do`
- **Official documentation:** [Get Amazon raw HTML](https://scrape.do/documentation/amazon-scraper-api/raw-html/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `geocode` | query | `string` | yes | Amazon marketplace country code such as us, gb, de, or jp. |
| `url` | query | `string` | yes | The full Amazon URL to fetch as raw HTML. |
| `zipcode` | query | `string` | yes | Postal code formatted for the selected marketplace. |
