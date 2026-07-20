# Outpaint Image with Dreamstudio

Expands an image beyond its borders in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/outpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Outpaint Image](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to outpaint. |
| `prompt` | body | `string` | no | Optional prompt that describes what to add around the expanded canvas. |
