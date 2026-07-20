# Terminate Calls by Call IDs with Ringg AI

Terminates active Ringg AI calls by call IDs.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaign/terminate`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Terminate Calls by Call IDs](https://docs.ringg.ai/api-reference/terminate/call-ids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | no | ID of the agent whose calls should be terminated |
| `call_ids[]` | body | `array<string>` | no | Array of call IDs to terminate |
| `campaign_id` | body | `string` | no | ID of the campaign whose calls should be terminated |
| `mobile_numbers[]` | body | `array<string>` | no | Array of mobile numbers to terminate calls for (max 100) |
