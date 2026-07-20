# List Charts with Microsoft 365 Excel

Retrieves charts from a worksheet in Microsoft 365 Excel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Charts](https://learn.microsoft.com/en-us/graph/api/worksheet-list-charts?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `worksheetName` | path | `string` | yes |
