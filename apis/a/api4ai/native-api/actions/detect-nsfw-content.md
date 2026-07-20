# Detect NSFW Content with api4ai

Detects NSFW content from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/nsfw/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Detect NSFW Content](https://api4.ai/docs/nsfw)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
