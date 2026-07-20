# Create Agent with Beyond Presence

Creates a new agent in Beyond Presence.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents`
- **Base URL:** `https://api.bey.dev`
- **Official documentation:** [Create Agent](https://docs.bey.dev/api-reference/agents/create-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatar_id` | body | `string` | yes | ID of avatar to use. |
| `name` | body | `string` | yes | Display name to use. |
| `system_prompt` | body | `string` | yes | System prompt to use. |
