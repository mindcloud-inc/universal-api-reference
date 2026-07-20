# Reverse Geocode Coordinate with Geocodio

Retrieves address details from Geocodio for one coordinate.

## Endpoint

- **Method:** `GET`
- **Path:** `/reverse`
- **Base URL:** `https://api.geocod.io/v1.12`
- **Official documentation:** [Reverse Geocode Coordinate](https://www.geocod.io/docs/#reverse-geocoding-single-coordinate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Latitude and longitude to reverse geocode, formatted as lat,lng. |
| `fields` | query | `string` | no | Optional comma-separated list of data append fields. Send multiple values as a string separated by `,`. |
| `skipGeocoding` | query | `boolean` | no | When present, extracts field data from coordinates without reverse geocoding. |
