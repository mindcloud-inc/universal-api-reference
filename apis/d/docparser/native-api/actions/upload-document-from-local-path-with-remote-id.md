# Upload Document From Local Path With Remote ID with Docparser

Uploads a local document to a Docparser parser and assigns a remote ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/document/upload/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Upload Document From Local Path With Remote ID](https://docparser.com/api/#upload-document-from-local-path)

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
| `remote_id` | body | `string` | yes |
