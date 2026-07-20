# Sort Sheet Rows with Smartsheet

Sorts rows in a Smartsheet sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/sheets/:sheetId/sort`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Sort Sheet Rows](https://developers.smartsheet.com/api/smartsheet/openapi/rows/sort-rows)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `sortCriteria[]` | body | `array<object>` | yes |
