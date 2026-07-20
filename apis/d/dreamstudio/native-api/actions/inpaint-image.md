# Inpaint Image with Dreamstudio

Fills masked regions in an image in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/inpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Inpaint Image](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to inpaint. |
| `prompt` | body | `string` | yes | Prompt describing the desired inpainted result. |
