# Set Post-Call Outcome with Phonely

Updates a post-call outcome in Phonely.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/calls/{{agentId}}/{{callIdOrPhone}}`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Set Post-Call Outcome](https://docs.phonely.ai/api-reference/endpoint/set-post-call-outcome)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | path | `string` | yes |
| `callIdOrPhone` | path | `string` | yes |
| `custom_call_outcome` | body | `string` | no |
| `custom_call_outcome_value` | body | `number` | no |
| `custom_call_metadata` | body | `object` | no |
