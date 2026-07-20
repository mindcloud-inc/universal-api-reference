# Continue Agent Run with Toolhouse

## Endpoint

- **Method:** `PUT`
- **Path:** `/agent-runs/:run_id`
- **Base URL:** `https://api.toolhouse.ai/v1`
- **Official documentation:** [Continue Agent Run](https://docs.toolhouse.ai/toolhouse/agent-workers/running-agents-asynchronously/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | The follow-up message to continue the agent run with. |
| `run_id` | path | `string` | yes | The agent run ID. |
