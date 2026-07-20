# Clear Range with Microsoft 365 Excel

Clears a worksheet range in Microsoft 365 Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')/clear`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Clear Range](https://learn.microsoft.com/en-us/graph/api/range-clear?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `worksheetName` | path | `string` | yes |
| `startCell` | path | `string` | yes |
| `endCell` | path | `string` | yes |
| `applyTo` | body | `string` | no |
