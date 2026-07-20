# Search Redfin Listings with HasData

Retrieves Redfin listings from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/redfin/listing`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Redfin Listings](https://docs.hasdata.com/apis/redfin/listing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Zip code or area to search on Redfin. |
| `page` | query | `number` | no | Page number of Redfin listing results. |
| `type` | query | `string` | yes | Listing type, such as forSale. |
