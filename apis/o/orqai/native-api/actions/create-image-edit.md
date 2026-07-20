# Create Image Edit with Orq.ai

Creates an image edit in Orq.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/router/images/edits`
- **Base URL:** `https://api.orq.ai`
- **Official documentation:** [Create Image Edit](https://docs.orq.ai/reference/images/create-image-edit)

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
| `prompt` | body | `string` | yes |
