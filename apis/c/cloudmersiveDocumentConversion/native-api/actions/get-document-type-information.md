# Get Document Type Information with Cloudmersive Document Conversion

Retrieves document type information in Cloudmersive Document Conversion.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/autodetect/get-info`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Get Document Type Information](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input file to identify and inspect. |
