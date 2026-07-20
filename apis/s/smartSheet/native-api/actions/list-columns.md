# List Columns with Smartsheet

Retrieves columns from a Smartsheet sheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetId/columns`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [List Columns](https://developers.smartsheet.com/api/smartsheet/openapi/columns/columns-listonsheet)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `level` | query | `number` | no |
| `includeAll` | query | `boolean` | no |
