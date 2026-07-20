# Add Preset with PixelBin.io

Creates a new preset in PixelBin.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/presets`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Add Preset](https://www.pixelbin.io/docs/presets/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `presetName` | body | `string` | yes |
| `transformation` | body | `string` | yes |
