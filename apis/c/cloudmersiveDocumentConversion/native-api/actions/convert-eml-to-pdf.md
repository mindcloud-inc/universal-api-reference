# Convert Email EML to PDF with Cloudmersive Document Conversion

Converts an email EML file to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/eml/to/pdf`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Email EML to PDF](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input EML email file to convert to PDF. |
