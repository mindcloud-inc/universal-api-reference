# Update Agent with Beyond Presence

Updates an existing agent in Beyond Presence.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/agents/:id`
- **Base URL:** `https://api.bey.dev`
- **Official documentation:** [Update Agent](https://docs.bey.dev/api-reference/agents/update-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatar_id` | body | `string` | no | — |
| `greeting` | body | `string` | no | — |
| `id` | path | `string` | yes | Agent ID. |
| `language` | body | `string` | no | — |
| `max_session_length_minutes` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `system_prompt` | body | `string` | no | — |
