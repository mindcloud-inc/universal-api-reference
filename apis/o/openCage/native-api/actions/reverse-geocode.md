# Reverse Geocode with OpenCage

Retrieves location details from OpenCage by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/json`
- **Base URL:** `https://api.opencagedata.com/geocode/v1`
- **Official documentation:** [Reverse Geocode](https://opencagedata.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Latitude and longitude in decimal format, in latitude,longitude order. |
| `language` | query | `string` | no | Optional language code to favor in returned results, such as `de`, `pt-BR`, or `native`. |
| `address_only` | query | `string` | no | Optional flag. Set to `1` to include only the address in the formatted string when possible. |
| `roadinfo` | query | `string` | no | Optional flag. Set to `1` to match the nearest road and include road information when possible. |
