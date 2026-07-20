# Create Image Variation with Orq.ai

Creates an image variation in Orq.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/router/images/variations`
- **Base URL:** `https://api.orq.ai`
- **Official documentation:** [Create Image Variation](https://docs.orq.ai/reference/images/create-image-variation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `image` | body | `file` | yes |
| `model` | body | `string` | yes |
