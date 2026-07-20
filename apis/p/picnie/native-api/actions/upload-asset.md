# Upload Asset with Picnie

Uploads an image asset to Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload-asset`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Upload Asset](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Public image URL to download and upload into Picnie when running through MindCloud. |
