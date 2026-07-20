# List Google Maps Reviews with HasData

Retrieves Google Maps reviews from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/google-maps/reviews`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [List Google Maps Reviews](https://docs.hasdata.com/apis/google-maps/reviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataId` | query | `string` | no | Google Maps data ID. Either Data ID or Place ID should be set. |
| `nextPageToken` | query | `string` | no | Token for the next page of reviews. |
| `placeId` | query | `string` | no | Google Maps place ID. Either Data ID or Place ID should be set. |
| `sortBy` | query | `string` | no | Sorting option for reviews. |
