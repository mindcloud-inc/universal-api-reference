# Convert PowerPoint PPTX to PDF with Cloudmersive Document Conversion

Converts a PowerPoint PPTX presentation to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/pptx/to/pdf`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert PowerPoint PPTX to PDF](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input PowerPoint PPTX presentation to convert to PDF. |
