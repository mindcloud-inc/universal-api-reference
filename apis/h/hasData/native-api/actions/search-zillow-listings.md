# Search Zillow Listings with HasData

Retrieves Zillow listings from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/zillow/listing`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Zillow Listings](https://docs.hasdata.com/apis/zillow/listing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Location keyword or area for Zillow listings. |
| `page` | query | `number` | no | Page number of Zillow listing results. |
| `sort` | query | `string` | no | Sort order for Zillow listings. |
| `type` | query | `string` | yes | Listing type, such as forSale. |
