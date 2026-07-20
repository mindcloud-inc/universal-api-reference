# Create Agent with Synthflow AI Phone Calling

Creates a new voice agent in Synthflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/assistants`
- **Base URL:** `https://api.synthflow.ai/v2`
- **Official documentation:** [Create Agent](https://docs.synthflow.ai/api-reference/platform-api/agents/create-assistant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | body | `object` | yes | Agent configuration object. |
| `name` | body | `string` | yes | Agent name. |
| `type` | body | `string` | yes | Agent type such as outbound, inbound, or widget. |
