# Detect NSFW Content from File with api4ai

Detects NSFW content from an image file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/nsfw/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Detect NSFW Content from File](https://api4.ai/docs/nsfw)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to classify for NSFW content. |
