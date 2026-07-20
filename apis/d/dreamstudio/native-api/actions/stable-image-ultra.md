# Stable Image Ultra with Dreamstudio

Creates an image with Stable Image Ultra in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/generate/ultra`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Stable Image Ultra](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt used to generate the image. |
| `output_format` | body | `string` | no | Optional output file format for the generated image. |
