# Convert JSON To Excel with Encodian

Converts JSON data to Excel in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertJsonToExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert JSON To Excel](https://support.encodian.com/hc/en-gb/articles/7690520790045)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFilename` | body | `string` | yes | The filename including extension of the output document. |
| `fileContent` | body | `string` | no | Optional base64 encoded representation of the JSON file to process. |
| `jsonData` | body | `string` | no | Optional JSON data string to process. |
| `firstRow` | body | `number` | no | The first row to be written to. |
| `firstColumn` | body | `number` | no | The first column to be written to. |
| `worksheetName` | body | `string` | no | The worksheet name that the JSON data is added to. |
| `convertNumericAndDate` | body | `boolean` | no | Auto parse numeric and date values and set matching cell formats. |
| `dateFormat` | body | `string` | no | Custom date and time format string. |
| `numericFormat` | body | `string` | no | Numeric format string. |
| `ignoreNullValues` | body | `boolean` | no | Ignore JSON properties that contain null values. |
| `titleFontColor` | body | `string` | no | The title font color. |
| `titleFontBold` | body | `boolean` | no | Set the title text to bold. |
| `titleWrapText` | body | `boolean` | no | Set whether title text wraps. |
| `ignoreAttributeTitles` | body | `boolean` | no | Ignore JSON attribute titles in the output workbook. |
| `cultureName` | body | `string` | no | Set the workbook culture before conversion. |
