# List Table Rows with Microsoft 365 Excel

Retrieves rows from a Microsoft 365 Excel table.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/tables('{{tableName}}')/rows`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Table Rows](https://learn.microsoft.com/en-us/graph/api/table-list-rows?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `tableName` | path | `string` | yes |
