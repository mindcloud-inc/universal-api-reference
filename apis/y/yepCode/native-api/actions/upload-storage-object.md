# Upload storage object with YepCode

Creates a storage object in YepCode from a file.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/objects`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Upload storage object](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Storage/uploadStorageObject)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | Storage object filename, including optional folder path. |
| `file` | body | `file` | yes | File content to upload. |
