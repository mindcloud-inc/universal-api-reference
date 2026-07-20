# Convert HTML File to PDF with Cloudmersive Document Conversion

Converts an HTML file to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/html/to/pdf`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert HTML File to PDF](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input HTML document file to convert to PDF. |
