# Create Sheet with Smartsheet

Creates a new sheet in Smartsheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/sheets`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Create Sheet](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/create-sheet)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `columns[]` | body | `array<object>` | no |
| `fromId` | body | `number` | no |
| `include` | query | `string` | no |
