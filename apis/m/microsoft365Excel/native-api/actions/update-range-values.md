# Update Range Values with Microsoft 365 Excel

Updates worksheet range values in Microsoft 365 Excel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Update Range Values](https://learn.microsoft.com/en-us/graph/api/range-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes | Drive item ID of the Excel workbook file. |
| `worksheetName` | path | `string` | yes | Worksheet name exactly as it appears in the workbook, such as Sheet1 or Summary. |
| `startCell` | path | `string` | yes | Top-left cell in the target range, such as A1. |
| `endCell` | path | `string` | yes | Bottom-right cell in the target range, such as B3. |
| `values` | body | `object` | yes | Two-dimensional JSON array of cell values to write into the target range. |
