# List Worksheets with Microsoft 365

Retrieves worksheets from a Microsoft 365 workbook.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Worksheets](https://learn.microsoft.com/en-us/graph/api/worksheet-list?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes | Drive item ID of the Excel workbook file. |
