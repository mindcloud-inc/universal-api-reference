# Get Agent Response with Orq.ai

Retrieves an agent response from Orq.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/agents/[:agent_key]/responses/[:task_id]`
- **Base URL:** `https://api.orq.ai`
- **Official documentation:** [Get Agent Response](https://docs.orq.ai/reference/agents/get-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_key` | path | `string` | yes | Agent Key from the Orq.ai path parameter. |
| `task_id` | path | `string` | yes | Task ID from the Orq.ai path parameter. |
