# Upscale Image with api4ai

Upscales an image from a URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/image-upscale/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Upscale Image](https://api4.ai/docs/image-upscale)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to upscale. |
