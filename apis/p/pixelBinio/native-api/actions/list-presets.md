# List Presets with PixelBin.io

Retrieves preset records from your PixelBin.io account.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/presets`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [List Presets](https://www.pixelbin.io/docs/presets/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Filter presets by archive state. |
| `name` | query | `string` | no | Filter presets by name. |
| `pageNo` | query | `number` | no | Preset results page number. |
| `pageSize` | query | `number` | no | Preset results page size. |
| `transformation` | query | `string` | no | Filter presets by transformation chain. |
