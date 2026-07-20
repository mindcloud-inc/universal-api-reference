# Create Preset with Api2Convert

Creates a new preset in Api2Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/presets`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Create Preset](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the preset. |
| `target` | body | `string` | yes | Conversion target for the preset. |
| `scope` | body | `string` | yes | Preset visibility scope. Accepted values: `0`, `1`. |
| `options` | body | `object` | yes | Conversion options to store in the preset. |
