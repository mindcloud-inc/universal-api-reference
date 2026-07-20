# Convert - JSON to Excel with Encodian - Convert

Creates an Excel file from JSON in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertJsonToExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - JSON to Excel](https://support.encodian.com/hc/en-gb/articles/7690520790045)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFilename` | body | `string` | yes | The filename of the output Excel workbook. |
| `jsonData` | body | `string` | no | Raw JSON content to convert. |
| `fileContent` | body | `file` | no | JSON file content to convert. |
