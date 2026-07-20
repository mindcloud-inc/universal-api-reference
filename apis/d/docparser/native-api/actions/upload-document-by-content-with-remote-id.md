# Upload Document By Content With Remote ID with Docparser

Uploads document content to a Docparser parser and assigns a remote ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/document/upload/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Upload Document By Content With Remote ID](https://docparser.com/api/#upload-document-by-content)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes |
| `file_content` | body | `string` | yes |
| `file_name` | body | `string` | yes |
| `remote_id` | body | `string` | yes |
