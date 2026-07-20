# Convert Coordinates to what3words Address with What3Words

Retrieves a what3words address from coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/convert-to-3wa`
- **Base URL:** `https://api.what3words.com/v3`
- **Official documentation:** [Convert Coordinates to what3words Address](https://developer.what3words.com/public-api/docs#convert-to-3-word-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coordinates` | query | `string` | yes | Latitude and longitude separated by a comma, for example 51.521251,-0.203586. |
| `language` | query | `string` | no | Supported what3words language code. Defaults to English when omitted. |
| `format` | query | `list<string>` | no | Response format: json or geojson. Accepted values: `geojson`, `json`. |
| `locale` | query | `string` | no | Optional locale or script-specific code such as mn_la, zh_tr, or oo_la. |
