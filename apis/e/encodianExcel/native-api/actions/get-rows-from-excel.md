# Excel - Extract Rows with Encodian - Excel

Retrieves rows from an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/GetRowsFromExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Extract Rows](https://support.encodian.com/hc/en-gb/articles/9390845334172)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `worksheetName` | body | `string` | no |
| `hasHeaderRow` | body | `boolean` | no |
| `firstRow` | body | `number` | no |
| `lastRow` | body | `number` | no |
