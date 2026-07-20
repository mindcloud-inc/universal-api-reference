# Search Maps with Apple Map Links

Searches Apple Maps for places or addresses.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Search Maps](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search string, such as a POI category, address, or city name. |
| `center` | query | `string` | no | Optional search center as a comma-separated latitude,longitude coordinate pair. |
| `span` | query | `string` | no | Optional search area span as latitudeDelta,longitudeDelta. |
