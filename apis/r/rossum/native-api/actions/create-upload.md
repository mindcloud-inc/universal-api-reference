# Create Upload with Rossum

Uploads a document to a Rossum queue.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Upload](https://rossum.app/api/docs/openapi/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queue` | query | `number` | yes | Numeric queue ID that should receive the uploaded file. |
| `content` | body | `file` | yes | File content to upload to Rossum. |
| `metadata` | body | `string` | no | Optional JSON string with annotation metadata. |
