# Recognize Alcohol Content from File with api4ai

Recognizes alcohol labels from an image file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/alco-rec/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Recognize Alcohol Content from File](https://api4.ai/docs/alco-rec)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to analyze. |
