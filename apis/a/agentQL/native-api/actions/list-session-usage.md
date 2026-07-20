# List Session Usage with AgentQL

Retrieves Tetra browser session usage from AgentQL.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tetra/usage`
- **Base URL:** `https://api.agentql.com`
- **Official documentation:** [List Session Usage](https://docs.agentql.com/rest-api/api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sub_user_id` | query | `string` | no |
| `session_id` | query | `string` | no |
| `start_after` | query | `date` | no |
| `end_before` | query | `date` | no |
| `status` | query | `string` | no |
