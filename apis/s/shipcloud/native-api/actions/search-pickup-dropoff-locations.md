# Search Pickup Dropoff Locations with Shipcloud

Finds pickup dropoff locations in Shipcloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/pickup_dropoff_locations`
- **Base URL:** `https://api.shipcloud.io/v1`
- **Official documentation:** [Search Pickup Dropoff Locations](https://developers.shipcloud.io/swagger-ui/#/default/get_pickup_dropoff_locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carriers` | query | `string` | no | Restrict the search to one or more carriers. |
| `city` | query | `string` | no | City for address-based pickup/dropoff search. |
| `country` | query | `string` | no | ISO country code for address-based pickup/dropoff search. |
| `latitude` | query | `number` | no | Latitude for coordinate-based pickup/dropoff search. |
| `limit` | query | `number` | no | Maximum number of pickup/dropoff locations to return. |
| `longitude` | query | `number` | no | Longitude for coordinate-based pickup/dropoff search. |
| `radius` | query | `number` | no | Search radius around the coordinates. |
| `state` | query | `string` | no | State or region for address-based pickup/dropoff search. |
| `street` | query | `string` | no | Street for address-based pickup/dropoff search. |
| `zip_code` | query | `string` | no | ZIP or postal code for address-based pickup/dropoff search. |
