# Disable Agent with OnceOnly

Disables an agent in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/:agent_id/disable`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Disable Agent](https://docs.onceonly.tech/reference/agents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | Agent id to disable. |
| `reason` | body | `string` | no | Optional disable reason. |
