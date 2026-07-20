# Upload storage object raw with YepCode

Creates a storage object in YepCode from raw content.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/objects`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Upload storage object raw](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Storage/uploadStorageObject)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | Storage object filename, including optional folder path. |
| `content` | body | `string` | yes | Raw file contents to upload. |
