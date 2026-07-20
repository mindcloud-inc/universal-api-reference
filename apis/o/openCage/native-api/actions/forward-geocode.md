# Forward Geocode with OpenCage

Finds location details in OpenCage by address or place name.

## Endpoint

- **Method:** `GET`
- **Path:** `/json`
- **Base URL:** `https://api.opencagedata.com/geocode/v1`
- **Official documentation:** [Forward Geocode](https://opencagedata.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Address, place name, or LOCODE query to geocode. Must be at least two characters. |
| `limit` | query | `number` | no | Maximum number of results to return for forward geocoding. Defaults to 10 and can be up to 100. |
| `countrycode` | query | `string` | no | Optional ISO 3166-1 alpha-2 country code, or comma-separated country codes, to restrict forward geocoding results. |
| `bounds` | query | `string` | no | Optional bounding box for forward geocoding in min longitude, min latitude, max longitude, max latitude order. |
| `language` | query | `string` | no | Optional language code to favor in returned results, such as `de`, `pt-BR`, or `native`. |
| `proximity` | query | `string` | no | Optional latitude,longitude hint to bias forward geocoding results toward a location. |
