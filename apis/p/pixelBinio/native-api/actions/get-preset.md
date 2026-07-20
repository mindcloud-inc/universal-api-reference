# Get Preset with PixelBin.io

Retrieves a preset from PixelBin.io by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/presets/:presetName`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Get Preset](https://www.pixelbin.io/docs/presets/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presetName` | path | `string` | yes | Preset name returned by List Presets or created during verification. |
