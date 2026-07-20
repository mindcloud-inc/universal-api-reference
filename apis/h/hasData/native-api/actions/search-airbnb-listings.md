# Search Airbnb Listings with HasData

Retrieves Airbnb listings from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/airbnb/listing`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Airbnb Listings](https://docs.hasdata.com/apis/airbnb/listing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkIn` | query | `string` | yes | Check-in date in YYYY-MM-DD format. |
| `checkOut` | query | `string` | no | Check-out date in YYYY-MM-DD format. |
| `location` | query | `string` | yes | Location to search for Airbnb listings. |
| `nextPageToken` | query | `string` | no | Token for the next page of Airbnb listings. |
