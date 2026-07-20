# Delete Rows with Smartsheet

Deletes rows from a Smartsheet sheet.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sheets/:sheetId/rows`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Delete Rows](https://developers.smartsheet.com/api/smartsheet/openapi/rows/delete-rows)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `ids` | query | `string` | yes |
| `ignoreRowsNotFound` | query | `boolean` | no |
