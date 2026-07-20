# Update Worksheet with Microsoft 365 Excel

Updates a worksheet in a Microsoft 365 Excel workbook.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Update Worksheet](https://learn.microsoft.com/en-us/graph/api/worksheet-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `worksheetName` | path | `string` | yes |
| `name` | body | `string` | no |
| `visibility` | body | `string` | no |
