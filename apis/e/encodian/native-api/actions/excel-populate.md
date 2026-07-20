# Excel Populate with Encodian

Populates an Excel workbook in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/PopulateExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel Populate](https://support.encodian.com/hc/en-gb/articles/12736409527324)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | The Microsoft Excel file (XLSX) to populate. |
| `jsonData` | body | `string` | yes | The JSON data to populate the Microsoft Excel file with. |
| `jsonParseMode` | body | `string` | no | Sets how JSON simple values are parsed. |
| `calculateWorkbook` | body | `boolean` | no | Recalculate Excel formulas before returning the workbook. |
| `useExcelDataTypes` | body | `boolean` | no | Use Excel data types for generated values. |
| `allowMissingValues` | body | `boolean` | no | Allow missing values within the JSON data. |
| `inlineErrors` | body | `boolean` | no | Produce errors within the resultant file instead of returning an HTTP 4xx response. |
| `removeEmptyParagraphs` | body | `boolean` | no | Automatically remove empty paragraphs upon execution. |
| `dateTimeFormats` | body | `string` | no | One or more specific formats for parsing DateTime values. |
| `cultureName` | body | `string` | no | Set the culture for the workbook prior to conversion. |
