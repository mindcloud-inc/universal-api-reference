# Geocode Location with GraphHopper

Retrieves geocoding results for a query in GraphHopper.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Geocode Location](https://docs.graphhopper.com/openapi/geocoding/getgeocode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Address or place text to geocode. |
| `point` | query | `string` | no | Latitude,longitude point for reverse geocoding. |
| `reverse` | query | `boolean` | no | Whether to reverse geocode the supplied point. |
| `limit` | query | `number` | no | Maximum number of geocoding results to return. |
| `locale` | query | `string` | no | Locale of returned names. |
