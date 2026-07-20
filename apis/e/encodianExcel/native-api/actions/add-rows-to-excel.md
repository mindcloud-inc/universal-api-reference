# Excel - Add Rows with Encodian - Excel

Adds rows to an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/AddRowsToExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Add Rows](https://support.encodian.com/hc/en-gb/articles/11551842583581)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `jsonData` | body | `string` | yes |
| `worksheetName` | body | `string` | no |
| `tableName` | body | `string` | no |
