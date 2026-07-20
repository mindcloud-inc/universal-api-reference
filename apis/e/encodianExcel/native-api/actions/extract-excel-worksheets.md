# Excel - Extract Worksheets with Encodian - Excel

Extracts worksheets from an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ExtractExcelWorksheets`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Extract Worksheets](https://support.encodian.com/hc/en-gb/articles/13230802892316)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `worksheetNames` | body | `string` | no |
| `worksheetIndexes` | body | `string` | no |
