# Get Used Range with Microsoft 365 Excel

Retrieves the used range from a Microsoft 365 Excel worksheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/usedRange`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Used Range](https://learn.microsoft.com/en-us/graph/api/worksheet-usedrange?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `worksheetName` | path | `string` | yes |
