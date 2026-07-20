# Upload Custom Sources with Chat Aid

Uploads new custom sources to Chat Aid.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/sources/custom`
- **Base URL:** `https://api.chataid.com`
- **Official documentation:** [Upload Custom Sources](https://docs.chataid.com/api-guide/custom-sources)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `string` | no | Team ID for the uploaded source. Defaults to organization-wide when omitted. |
| `files` | body | `file` | yes | File to upload as a custom source. |
