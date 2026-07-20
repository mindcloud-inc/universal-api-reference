# Recognize Wine with api4ai

Recognizes wine labels from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/wine-rec/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Recognize Wine](https://api4.ai/docs/wine-rec)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
