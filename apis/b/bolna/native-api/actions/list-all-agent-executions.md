# List All Agent Executions with Bolna

Retrieves execution records for a specific Bolna agent.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/agent/:agentId/executions`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [List All Agent Executions](https://www.bolna.ai/docs/api-reference/agent/v2/get_all_agent_executions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The unique agent ID from Bolna. |
| `answered_by_voice_mail` | query | `boolean` | no | Optional voicemail filter. |
| `batch_id` | query | `string` | no | Optional batch ID filter. |
| `call_type` | query | `string` | no | Optional call-direction filter. |
| `from` | query | `date` | no | Optional lower UTC datetime bound for execution creation time. |
| `provider` | query | `string` | no | Optional conversation-provider filter. |
| `status` | query | `string` | no | Optional execution status filter. |
| `to` | query | `date` | no | Optional upper UTC datetime bound for execution creation time. |
