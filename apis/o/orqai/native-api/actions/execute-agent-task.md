# Execute Agent Task with Orq.ai

Executes an agent task in Orq.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/agents/[:agent_key]/task`
- **Base URL:** `https://api.orq.ai`
- **Official documentation:** [Execute Agent Task](https://docs.orq.ai/reference/agents/execute-an-agent-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_key` | path | `string` | yes | Agent Key from the Orq.ai path parameter. |
