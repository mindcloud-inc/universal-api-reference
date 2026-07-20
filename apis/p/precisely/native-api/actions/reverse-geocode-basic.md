# Reverse Geocode (Basic) with Precisely

Retrieves address details from Precisely for a coordinate.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode/v1/basic/reverseGeocode`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Reverse Geocode (Basic)](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geocode/ReverseGeocode/LI_revGeo_GET_desc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x` | query | `number` | yes | Longitude in degrees, for example: -79.391165. |
| `y` | query | `number` | yes | Latitude in degrees, for example: 43.643469. |
| `country` | query | `string` | no | ISO country code or country name. |
| `coordSysName` | query | `string` | no | Coordinate system to convert the geometry to, in codespace:code format, for example EPSG:4326. |
| `distance` | query | `number` | no | Search radius around the input coordinates. |
| `distanceUnits` | query | `string` | no | Unit of measurement for the search distance. |
