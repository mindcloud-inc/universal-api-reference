# Excel - Update Rows with Encodian - Excel

Updates rows in an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/UpdateRowsInExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Update Rows](https://support.encodian.com/hc/en-gb/articles/11205752671004)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `jsonData` | body | `string` | yes |
| `updateRow` | body | `number` | yes |
| `updateColumn` | body | `number` | yes |
| `worksheetName` | body | `string` | no |
