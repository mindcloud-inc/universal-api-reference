# Delete Worksheet with Microsoft 365 Excel

Deletes a worksheet from a Microsoft 365 Excel workbook.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Delete Worksheet](https://learn.microsoft.com/en-us/graph/api/worksheet-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `worksheetName` | path | `string` | yes |
