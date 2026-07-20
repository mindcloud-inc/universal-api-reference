# Detect Objects from File with api4ai

Detects objects from an image file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/general-det/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Detect Objects from File](https://api4.ai/docs/object-detection)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to analyze for objects. |
