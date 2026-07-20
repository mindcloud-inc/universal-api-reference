# Get Sheet with Smartsheet

Retrieves a sheet from Smartsheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetId`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Get Sheet](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/getsheet)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `include` | query | `string` | no |
| `exclude` | query | `string` | no |
| `columnIds` | query | `string` | no |
| `filterId` | query | `number` | no |
| `level` | query | `number` | no |
| `page` | query | `number` | no |
| `pageSize` | query | `number` | no |
| `rowIds` | query | `string` | no |
| `rowNumbers` | query | `string` | no |
| `rowsModifiedSince` | query | `date` | no |
