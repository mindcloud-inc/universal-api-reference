# Excel - Delete Rows with Encodian - Excel

Deletes rows from an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/DeleteRowsFromExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Delete Rows](https://support.encodian.com/hc/en-gb/articles/9936160309148)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | — |
| `rowArray` | body | `string` | yes | Runtime-verified Encodian row range format, for example [2-2] or [23-56],[100-120]. |
| `worksheetName` | body | `string` | no | — |
| `firstRow` | body | `number` | no | Documented by Encodian, but rowArray is the runtime-verified input format for this app. |
| `lastRow` | body | `number` | no | Documented by Encodian, but rowArray is the runtime-verified input format for this app. |
