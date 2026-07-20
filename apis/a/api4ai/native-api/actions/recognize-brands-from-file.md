# Recognize Brands from File with api4ai

Recognizes brands from an image file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/brand-det/v2/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Recognize Brands from File](https://api4.ai/docs/brand-recognition)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to analyze. |
