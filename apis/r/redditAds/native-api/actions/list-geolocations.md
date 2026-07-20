# List Geolocations with Reddit Lead Ads

Retrieves targetable geolocations from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/targeting/geolocations`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Geolocations](https://ads-api.reddit.com/docs/v3/operations/list-geolocations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cities_search` | query | `string` | no | Optional city search text. |
| `country` | query | `string` | no | Optional country filter. |
| `postal_code` | query | `string` | no | Optional postal code filter. |
