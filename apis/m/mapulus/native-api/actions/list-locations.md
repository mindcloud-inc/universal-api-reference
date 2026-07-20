# List Locations with Mapulus

Retrieves locations from your Mapulus account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/locations`
- **Base URL:** `https://api.mapulus.com`
- **Official documentation:** [List Locations](https://developer.mapulus.com/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `map_id` | query | `string` | no | Filter locations by map ID. |
| `layer_id` | query | `string` | no | Filter locations by layer ID. |
| `external_id` | query | `string` | no | Filter locations by external ID. |
| `nearest[lat]` | query | `number` | no | Latitude for nearest-location search. |
| `nearest[lon]` | query | `number` | no | Longitude for nearest-location search. |
| `nearest[address]` | query | `string` | no | Address for nearest-location search. |
| `nearest[sort_by]` | query | `string` | no | Sort nearest results by distance or time. |
| `nearest[profile]` | query | `string` | no | Routing profile for nearest-location search. |
| `nearest[live_traffic]` | query | `string` | no | Whether to include live traffic in nearest-location search. |
| `nearest[limit]` | query | `number` | no | Limit nearest-location results. |
