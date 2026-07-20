# Convert ODT to DOCX with Cloudmersive Document Conversion

Converts an ODT file to DOCX.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/odt/to/docx`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert ODT to DOCX](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input ODT text document to convert to DOCX. |
