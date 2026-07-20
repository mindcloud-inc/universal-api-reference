# Upload Image with Sharetribe

Uploads an image to Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `images/upload`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Upload Image](https://www.sharetribe.com/api-reference/integration.html#upload-image)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | The image file to upload. |
