# Get Google Maps Place Details with ScrapingDog

Retrieves Google Maps place details through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/google_maps/places`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Get Google Maps Place Details](https://docs.scrapingdog.com/google-maps-api/google-maps-places-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_id` | query | `string` | yes | Google Maps data_id value for the place to fetch. |
