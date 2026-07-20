# Create Agent Run with Toolhouse

## Endpoint

- **Method:** `POST`
- **Path:** `/agent-runs`
- **Base URL:** `https://api.toolhouse.ai/v1`
- **Official documentation:** [Create Agent Run](https://docs.toolhouse.ai/toolhouse/agent-workers/running-agents-asynchronously/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundle` | body | `string` | no | Optional Toolhouse bundle name. |
| `callback_url` | body | `string` | no | Optional webhook URL to receive completion callbacks. |
| `chat_id` | body | `string` | yes | The Toolhouse chat ID to run. |
| `toolhouse_id` | body | `string` | no | Optional Toolhouse workspace identifier. |
| `vars` | body | `object` | no | Variables passed to the agent run. |
