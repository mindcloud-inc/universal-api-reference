# Delete Column with Smartsheet

Deletes an existing column from a Smartsheet sheet.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sheets/:sheetId/columns/:columnId`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Delete Column](https://developers.smartsheet.com/api/smartsheet/openapi/columns/delete-column)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `columnId` | path | `number` | yes |
