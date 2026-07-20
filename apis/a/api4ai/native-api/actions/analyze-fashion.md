# Analyze Fashion with api4ai

Analyzes fashion items from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/fashion/v2/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Analyze Fashion](https://api4.ai/docs/fashion)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
