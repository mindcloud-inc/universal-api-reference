# Analyze Face from File with api4ai

Analyzes a face from an image file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/face-analyzer/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Analyze Face from File](https://api4.ai/docs/face-analysis)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Face image file to analyze. |
