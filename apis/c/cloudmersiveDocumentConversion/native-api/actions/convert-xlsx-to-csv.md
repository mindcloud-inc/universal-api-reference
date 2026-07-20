# Convert Excel XLSX to CSV with Cloudmersive Document Conversion

Converts an Excel XLSX spreadsheet to CSV.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/xlsx/to/csv`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Excel XLSX to CSV](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input Excel XLSX spreadsheet to convert to CSV. |
