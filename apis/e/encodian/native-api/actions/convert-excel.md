# Convert Excel with Encodian

Converts an Excel file in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert Excel](https://support.encodian.com/hc/en-gb/articles/360011804178)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `outputFormat` | body | `string` | yes |
| `filename` | body | `string` | yes |
| `fileContent` | body | `string` | yes |
| `autoFit` | body | `boolean` | no |
| `worksheet` | body | `string` | no |
| `onePagePerSheet` | body | `boolean` | no |
| `allColumnsInOnePagePerSheetName` | body | `boolean` | no |
| `removeMarkup` | body | `boolean` | no |
| `exportHiddenSheets` | body | `boolean` | no |
| `csvDelimiter` | body | `string` | no |
| `cultureName` | body | `string` | no |
| `generateBookmarks` | body | `boolean` | no |
| `pdfACompliant` | body | `boolean` | no |
| `pdfAComplianceLevel` | body | `string` | no |
| `compression` | body | `string` | no |
