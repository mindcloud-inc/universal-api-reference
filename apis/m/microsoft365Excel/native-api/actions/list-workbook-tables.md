# List Workbook Tables with Microsoft 365 Excel

Retrieves tables from a Microsoft 365 Excel workbook.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/:siteId/drive/items/:driveItemId/workbook/tables`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Workbook Tables](https://learn.microsoft.com/en-us/graph/api/workbook-list-tables?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | SharePoint site ID for the workbook file. |
| `driveItemId` | path | `string` | yes | Drive item ID of the Excel workbook file. |
