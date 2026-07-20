# Convert Excel XLSX to HTML with Cloudmersive Document Conversion

Converts an Excel XLSX spreadsheet to HTML.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/xlsx/to/html`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Excel XLSX to HTML](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input Excel XLSX spreadsheet to convert to HTML. |
