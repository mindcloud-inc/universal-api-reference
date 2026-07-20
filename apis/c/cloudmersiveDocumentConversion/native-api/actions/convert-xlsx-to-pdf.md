# Convert Excel XLSX to PDF with Cloudmersive Document Conversion

Converts an Excel XLSX spreadsheet to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/xlsx/to/pdf`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Excel XLSX to PDF](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input Excel XLSX spreadsheet to convert to PDF. |
