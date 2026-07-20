# Enable/Disable Agent Integration with Chatvolt AI

Enables or disables an agent integration in Chatvolt AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agents/{id}/webhook`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Enable/Disable Agent Integration](https://docs.chatvolt.ai/api-reference/endpoint/agents/webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the agent to which the service provider belongs. |
| `type` | query | `string` | yes | Type of the service provider for which the webhook status will be changed. |
| `enabled` | query | `boolean` | yes | Defines the new webhook status. `true` to enable, `false` to disable. |
