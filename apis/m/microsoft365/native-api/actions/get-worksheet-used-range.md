# Get Worksheet Used Range with Microsoft 365

Retrieves a worksheet's used range from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/usedRange()`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Get Worksheet Used Range](https://learn.microsoft.com/en-us/graph/api/worksheet-usedrange?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes | Microsoft Graph drive item ID for the Excel workbook. |
| `worksheetName` | path | `string` | yes | Name of the worksheet to read. |
