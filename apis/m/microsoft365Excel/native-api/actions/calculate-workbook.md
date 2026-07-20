# Calculate Workbook with Microsoft 365 Excel

Calculates formulas in a Microsoft 365 Excel workbook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/application/calculate`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Calculate Workbook](https://learn.microsoft.com/en-us/graph/api/workbookapplication-calculate?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
| `calculationType` | body | `string` | yes |
