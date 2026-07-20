# Upload File Source with Chatsistant

Creates a new file source in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/data-source/upload`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Upload File Source](https://docs.chatsistant.com/api-reference/data-sources/create-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File input for multipart upload. The platform runner accepts base64 payloads, binary content, or fetchable URLs and sends the decoded file as the file field. |
| `meta_json` | body | `string` | no | JSON string sent in the meta_json multipart field, including reference_source_link when needed. |
| `uuid` | path | `string` | yes | The chatbot UUID. |
