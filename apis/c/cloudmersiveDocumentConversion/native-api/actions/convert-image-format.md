# Convert Image Format with Cloudmersive Document Conversion

Converts an image between formats in Cloudmersive Document Conversion.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/image/{format1}/to/{format2}`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Image Format](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format1` | path | `string` | yes | Input file format as a file extension, or UNKNOWN for unknown file formats. |
| `format2` | path | `string` | yes | Output file format as a file extension. |
| `inputFile` | body | `file` | yes | Input image file to convert. |
