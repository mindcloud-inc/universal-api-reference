# Style Guide Control with Dreamstudio

Creates an image using a style guide in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/control/style`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Style Guide Control](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt describing the generated image. |
| `image` | body | `file` | yes | Style guide image used to influence the generated output. |
