# Reverse Geocode to City with BigDataCloud

Reverse geocodes coordinates to a city in BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/reverse-geocode`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Reverse Geocode to City](https://www.bigdatacloud.com/reverse-geocoding/reverse-geocode-to-city-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | no | Latitude value in the WGS 84 reference system. |
| `longitude` | query | `number` | no | Longitude value in the WGS 84 reference system. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
