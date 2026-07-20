# Get Range with Microsoft 365 Excel

Retrieves a worksheet range from Microsoft 365 Excel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Range](https://learn.microsoft.com/en-us/graph/api/range-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `worksheetName` | path | `string` | yes |
| `startCell` | path | `string` | yes |
| `endCell` | path | `string` | yes |
