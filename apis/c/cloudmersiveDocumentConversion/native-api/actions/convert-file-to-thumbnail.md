# Convert File to Thumbnail with Cloudmersive Document Conversion

Converts a file to a thumbnail in Cloudmersive Document Conversion.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/autodetect/to/thumbnail`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert File to Thumbnail](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input file to automatically detect and convert to a PNG thumbnail. |
