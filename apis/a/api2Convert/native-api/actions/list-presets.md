# List Presets with Api2Convert

Retrieves available conversion presets from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/presets`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [List Presets](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Filter presets by category. |
| `target` | query | `string` | no | Filter presets by target format. |
| `filter` | query | `string` | no | Preset visibility filter supported by the Api2Convert API. |
