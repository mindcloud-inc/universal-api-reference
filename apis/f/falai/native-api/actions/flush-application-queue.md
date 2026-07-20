# Flush Application Queue with fal.ai

Deletes pending requests from a fal.ai application queue.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/serverless/apps/:owner/:name/queue`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Flush Application Queue](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Serverless app name. |
| `owner` | path | `string` | yes | App owner name. |
