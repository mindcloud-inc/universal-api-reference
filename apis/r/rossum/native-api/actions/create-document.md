# Create Document with Rossum

Creates a new document in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Document](https://rossum.app/api/docs/openapi/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `file` | yes | The file to upload. |
