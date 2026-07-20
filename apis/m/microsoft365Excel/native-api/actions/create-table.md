# Create Table with Microsoft 365 Excel

Creates a table in a Microsoft 365 Excel worksheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/tables/add`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Table](https://learn.microsoft.com/en-us/graph/api/tablecollection-add?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveItemId` | path | `string` | yes | — |
| `worksheetName` | path | `string` | yes | — |
| `address` | body | `string` | yes | The range address to convert into a table, for example RuntimeVerify!A1:B2. |
| `hasHeaders` | body | `boolean` | yes | — |
