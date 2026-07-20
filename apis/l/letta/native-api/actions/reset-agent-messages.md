# Reset Agent Messages with Letta

Resets an agent's messages in Letta.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/agents/:agent_id/reset-messages`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Reset Agent Messages](https://docs.letta.com/api/resources/agents/subresources/messages/methods/reset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
