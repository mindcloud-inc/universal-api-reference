# Create Worksheet in Workbook with Microsoft 365 Excel

Creates a worksheet in a Microsoft 365 Excel workbook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets/add`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Worksheet in Workbook](https://learn.microsoft.com/en-us/graph/api/worksheetcollection-add?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes | Drive item ID of the workbook file. |
| `name` | body | `string` | yes | — |
