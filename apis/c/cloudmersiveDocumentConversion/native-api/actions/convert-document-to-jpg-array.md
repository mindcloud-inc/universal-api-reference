# Convert Document to JPG Array with Cloudmersive Document Conversion

Converts a document to JPG images in Cloudmersive Document Conversion.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/autodetect/to/jpg`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Document to JPG Array](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input file to automatically detect and convert to JPG pages. |
