# Excel Extract Rows with Encodian

Extracts Excel rows in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/GetRowsFromExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel Extract Rows](https://support.encodian.com/hc/en-gb/articles/9390845334172)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | A Base64 encoded representation of the Excel file to be processed. |
| `worksheetName` | body | `string` | no | Set the name of a specific worksheet to be exported. |
| `hasHeaderRow` | body | `boolean` | no | Set whether the worksheet has a header row. |
| `firstRow` | body | `number` | no | Set the number of the first row to be exported. |
| `lastRow` | body | `number` | no | Set the number of the last row to be exported. |
| `firstColumn` | body | `number` | no | Set the number of the first column to be exported. |
| `lastColumn` | body | `number` | no | Set the number of the last column to be exported. |
| `excludeEmptyRows` | body | `boolean` | no | Set whether empty rows should be excluded from the export. |
| `exportEmptyCells` | body | `boolean` | no | Set whether empty cells should be exported. |
| `exportValuesAsText` | body | `boolean` | no | Set whether values should be exported as text. |
| `hyperlinkFormat` | body | `string` | no | Set how hyperlinks should be exported. |
| `exportAsObject` | body | `boolean` | no | Force row data to be exported as an object. |
| `excludeHiddenRows` | body | `boolean` | no | Set whether hidden rows should be excluded from the export. |
| `excludeHiddenColumns` | body | `boolean` | no | Set whether hidden columns should be excluded from the export. |
| `culture` | body | `string` | no | Set the culture for the workbook prior to conversion. |
