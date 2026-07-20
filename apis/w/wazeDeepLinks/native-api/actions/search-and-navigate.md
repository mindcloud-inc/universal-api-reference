# Search And Navigate with Waze Deep Links

Generates a Waze navigation URL from a search query.

## Endpoint

- **Method:** `GET`
- **Path:** `https://waze.com/ul`
- **Base URL:** `https://waze.com/ul`
- **Official documentation:** [Search And Navigate](https://developers.google.com/waze/deeplinks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Address or place to search in Waze. |
| `ll` | query | `string` | no | Optional latitude and longitude as lat,lng. |
