# Detect Objects with api4ai

Detects objects from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/general-det/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Detect Objects](https://api4.ai/docs/object-detection)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
