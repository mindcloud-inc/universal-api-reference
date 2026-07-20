# Create or Update Policy with OnceOnly

Creates or updates a policy in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/policies/:agent_id`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Create or Update Policy](https://docs.onceonly.tech/reference/policies/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | Agent id to update policy for. |
| `allowed_tools[]` | body | `array<string>` | no | Allowed tool names. |
| `blocked_tools[]` | body | `array<string>` | no | Blocked tool names. |
| `max_actions_per_hour` | body | `number` | no | Hourly action cap. |
| `max_spend_usd_per_day` | body | `number` | no | Daily spend cap in USD. |
