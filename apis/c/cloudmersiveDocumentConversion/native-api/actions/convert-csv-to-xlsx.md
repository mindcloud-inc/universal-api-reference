# Convert CSV to XLSX with Cloudmersive Document Conversion

Converts a CSV file to XLSX.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/csv/to/xlsx`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert CSV to XLSX](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input CSV file to convert to XLSX. |
