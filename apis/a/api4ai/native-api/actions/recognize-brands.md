# Recognize Brands with api4ai

Recognizes brands from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/brand-det/v2/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Recognize Brands](https://api4.ai/docs/brand-recognition)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
