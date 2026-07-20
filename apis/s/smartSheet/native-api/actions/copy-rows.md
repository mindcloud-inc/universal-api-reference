# Copy Rows with Smartsheet

Copies rows to another sheet in Smartsheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/sheets/:sheetId/rows/copy`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Copy Rows](https://developers.smartsheet.com/api/smartsheet/openapi/rows/copy-rows)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `rowIds[]` | body | `array<number>` | yes |
| `to` | body | `object` | yes |
| `include` | query | `string` | no |
| `ignoreRowsNotFound` | query | `boolean` | no |
