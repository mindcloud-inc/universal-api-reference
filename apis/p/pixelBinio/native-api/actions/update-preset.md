# Update Preset with PixelBin.io

Updates an existing preset in PixelBin.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/service/platform/assets/v1.0/presets/:presetName`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Update Preset](https://www.pixelbin.io/docs/presets/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `archived` | body | `boolean` | yes |
| `presetName` | path | `string` | yes |
