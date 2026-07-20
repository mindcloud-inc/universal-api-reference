# Add Chart with Microsoft 365 Excel

Creates a chart in a Microsoft 365 Excel worksheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts/add`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Add Chart](https://learn.microsoft.com/en-us/graph/api/chartcollection-add?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes | — |
| `worksheetName` | path | `string` | yes | — |
| `type` | body | `string` | yes | — |
| `sourceData` | body | `string` | yes | Range address for the chart source data, for example A1:B3. |
| `seriesBy` | body | `string` | no | — |
