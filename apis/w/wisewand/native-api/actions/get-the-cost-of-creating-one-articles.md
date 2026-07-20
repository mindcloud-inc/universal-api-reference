# Get the cost of creating one articles with Wisewand

Retrieves article creation cost from Wisewand.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/articles/cost`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Get the cost of creating one articles](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | The subject of the article. It can also contains source URLs. |
