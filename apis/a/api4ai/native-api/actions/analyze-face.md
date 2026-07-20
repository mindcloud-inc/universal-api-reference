# Analyze Face with api4ai

Analyzes a face from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/face-analyzer/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Analyze Face](https://api4.ai/docs/face-analysis)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
