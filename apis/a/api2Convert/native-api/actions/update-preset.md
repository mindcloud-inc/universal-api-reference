# Update Preset with Api2Convert

Updates an existing preset in Api2Convert.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/presets/:preset_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Update Preset](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preset_id` | path | `string` | yes | Unique identifier of the preset to update. |
| `body` | body | `object` | yes | Patch payload for the preset. |
