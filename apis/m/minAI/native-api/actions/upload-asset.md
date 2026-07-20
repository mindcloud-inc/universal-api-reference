# Upload asset with 1minAI

Uploads an asset file to 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/assets`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Upload asset](https://docs.1min.ai/docs/api/asset-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `asset` | body | `file` | yes |
