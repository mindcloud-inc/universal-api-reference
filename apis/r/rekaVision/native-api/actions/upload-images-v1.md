# Upload Images (V1) with Reka Vision

Uploads images to Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/upload`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Upload Images (V1)](https://docs.reka.ai/vision/api-reference/v-1/upload-images-v-1-images-upload-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `images[]` | body | `array<file>` | no |
| `metadata` | body | `string` | yes |
