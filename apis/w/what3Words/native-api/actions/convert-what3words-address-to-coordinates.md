# Convert what3words Address to Coordinates with What3Words

Retrieves coordinates from a what3words address.

## Endpoint

- **Method:** `GET`
- **Path:** `/convert-to-coordinates`
- **Base URL:** `https://api.what3words.com/v3`
- **Official documentation:** [Convert what3words Address to Coordinates](https://developer.what3words.com/public-api/docs#convert-to-coordinates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `words` | query | `string` | yes | The what3words address, such as filled.count.soap or ///filled.count.soap. |
| `format` | query | `list<string>` | no | Response format: json or geojson. Accepted values: `geojson`, `json`. |
