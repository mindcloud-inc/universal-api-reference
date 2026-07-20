# List Google Maps Reviews with ScrapingDog

Retrieves Google Maps reviews through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/google_maps/reviews`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [List Google Maps Reviews](https://docs.scrapingdog.com/google-maps-api/google-maps-reviews-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_id` | query | `string` | yes | Google Maps data_id value for the business or place. |
