# Detect Masks from File with api4ai

Detects face masks from an image file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/med-mask/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Detect Masks from File](https://api4.ai/apis/mask-detection)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Mask-detection image file to analyze. |
