# Recognize Alcohol Content with api4ai

Recognizes alcohol labels from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/alco-rec/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Recognize Alcohol Content](https://api4.ai/docs/alco-rec)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
