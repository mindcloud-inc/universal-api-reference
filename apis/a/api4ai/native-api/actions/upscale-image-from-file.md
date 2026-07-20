# Upscale Image from File with api4ai

Upscales an image from a file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/image-upscale/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Upscale Image from File](https://api4.ai/docs/image-upscale)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to upscale. |
