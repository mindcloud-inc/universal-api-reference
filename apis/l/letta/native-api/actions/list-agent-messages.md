# List Agent Messages with Letta

Retrieves messages from an agent in Letta.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agent_id/messages`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [List Agent Messages](https://docs.letta.com/api/resources/agents/subresources/messages/methods/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
