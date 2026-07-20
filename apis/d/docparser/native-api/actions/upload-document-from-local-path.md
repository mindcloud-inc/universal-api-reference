# Upload Document From Local Path with Docparser

Uploads a local document to a Docparser parser.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/document/upload/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Upload Document From Local Path](https://docparser.com/api/#upload-document-from-local-path)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes |
| `file` | body | `file` | yes |
