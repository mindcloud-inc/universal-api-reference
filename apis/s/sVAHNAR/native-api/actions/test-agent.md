# Test Agent with SVAHNAR

Tests an agent in SVAHNAR.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/test`
- **Base URL:** `https://api.svahnar.com`
- **Official documentation:** [Test Agent](https://docs.svahnar.com/docs/Agents/test_agent/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | The message or command to send to the test agent. |
| `yaml_string` | body | `string` | yes | YAML string to test the agent. |
| `thread_id` | body | `string` | no | Optional unique identifier for the chat session. |
| `agent_history` | body | `string` | no | Optional prior messages as a string payload. |
| `hitl_decision` | body | `list` | no | Optional human-in-the-loop decision. Accepted values: `approve`, `edit`, `reject`. |
