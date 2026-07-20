# Get Workbook Application with Microsoft 365 Excel

Retrieves workbook application details from Microsoft 365 Excel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/application`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Workbook Application](https://learn.microsoft.com/en-us/graph/api/workbookapplication-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes |
