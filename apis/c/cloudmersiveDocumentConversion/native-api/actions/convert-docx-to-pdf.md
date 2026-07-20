# Convert Word DOCX to PDF with Cloudmersive Document Conversion

Converts a Word DOCX document to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/docx/to/pdf`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Word DOCX to PDF](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input Word DOCX document to convert to PDF. |
