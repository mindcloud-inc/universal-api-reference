# Excel - Separate Worksheets with Encodian - Excel

Separates worksheets into individual files in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ExcelSeparateWorksheets`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Separate Worksheets](https://support.encodian.com/hc/en-gb/articles/21049256666908)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `cultureName` | body | `string` | no |
