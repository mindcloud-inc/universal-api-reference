# Excel - Delete Worksheets with Encodian - Excel

Deletes worksheets from an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/DeleteExcelWorksheets`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Delete Worksheets](https://support.encodian.com/hc/en-gb/articles/13233342312220)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `worksheetNames` | body | `string` | no |
| `worksheetIndexes` | body | `string` | no |
