# Get Queue Size with fal.ai

Retrieves queue size for a fal.ai application.

## Endpoint

- **Method:** `GET`
- **Path:** `/serverless/apps/:owner/:name/queue`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Get Queue Size](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Serverless app name. |
| `owner` | path | `string` | yes | App owner name. |
