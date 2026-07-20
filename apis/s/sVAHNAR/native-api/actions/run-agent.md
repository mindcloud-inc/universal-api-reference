# Run Agent with SVAHNAR

Runs an agent in SVAHNAR.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/run`
- **Base URL:** `https://api.svahnar.com`
- **Official documentation:** [Run Agent](https://docs.svahnar.com/docs/Agents/run_agent/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | yes | Unique identifier for the agent. |
| `message` | body | `string` | yes | The message or command to send to the agent. |
| `thread_id` | body | `string` | no | Optional unique identifier for the chat session. |
| `agent_history[]` | body | `array<object>` | no | Optional list of prior messages. |
| `hitl_decision` | body | `list` | no | Optional human-in-the-loop decision. Accepted values: `approve`, `edit`, `reject`. |
