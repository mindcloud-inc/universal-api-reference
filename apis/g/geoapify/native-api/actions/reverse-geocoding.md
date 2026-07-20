# Reverse Geocoding with Geoapify Geocode

Finds addresses in Geoapify by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode/reverse`
- **Base URL:** `https://api.geoapify.com/v1`
- **Official documentation:** [Reverse Geocoding](https://apidocs.geoapify.com/docs/geocoding/reverse-geocoding/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude coordinate of the target location. |
| `lon` | query | `number` | yes | Longitude coordinate of the target location. |
| `type` | query | `list<string>` | no | Restrict reverse results to a specific feature type. Accepted values: `amenity`, `city`, `country`, `postcode`, `state`, `street`. |
| `lang` | query | `string` | no | Result language using ISO 639-1 code. |
| `format` | query | `list` | no | Response format. Accepted values: `geojson`, `json`, `xml`. |
