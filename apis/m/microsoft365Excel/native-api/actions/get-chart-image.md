# Get Chart Image with Microsoft 365 Excel

Retrieves a chart image from Microsoft 365 Excel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts('{{chartName}}')/image(width={{width}},height={{height}},fittingMode='{{fittingMode}}')`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Chart Image](https://learn.microsoft.com/en-us/graph/api/chart-image?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `worksheetName` | path | `string` | yes |
| `chartName` | path | `string` | yes |
| `width` | path | `number` | yes |
| `height` | path | `number` | yes |
| `fittingMode` | path | `string` | yes |
