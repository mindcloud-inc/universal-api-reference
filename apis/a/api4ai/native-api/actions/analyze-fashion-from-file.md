# Analyze Fashion from File with api4ai

Analyzes fashion items from an image file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/fashion/v2/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Analyze Fashion from File](https://api4.ai/docs/fashion)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Fashion image file to analyze. |
