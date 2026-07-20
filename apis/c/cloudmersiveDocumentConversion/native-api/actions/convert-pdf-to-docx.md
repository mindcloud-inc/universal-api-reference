# Convert PDF to Word DOCX with Cloudmersive Document Conversion

Converts a PDF document to Word DOCX.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/pdf/to/docx`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert PDF to Word DOCX](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input PDF document to convert to Word DOCX. |
