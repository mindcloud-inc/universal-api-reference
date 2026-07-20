# Create and run a articles with Wisewand

Creates and runs an article in Wisewand.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/articles/`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Create and run a articles](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | The subject of the article. It can also contains source URLs. |
