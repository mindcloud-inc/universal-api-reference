# Add Table Rows with Microsoft 365 Excel

Adds rows to a Microsoft 365 Excel table.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/tables('{{tableName}}')/rows/add`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Add Table Rows](https://learn.microsoft.com/en-us/graph/api/table-post-rows?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes | — |
| `tableName` | path | `string` | yes | — |
| `values` | body | `object` | yes | Two-dimensional array of row values. |
| `index` | body | `number` | no | — |
