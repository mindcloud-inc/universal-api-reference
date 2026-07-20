# Update Squad with Vapi

Updates an existing squad in Vapi.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/squad/:id`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Update Squad](https://docs.vapi.ai/api-reference/squads/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | This is the name of the squad. |
| `members[]` | body | `array<object>` | yes | This is the list of assistants that make up the squad.  The call will start with the first assistant in the list. |
| `members[]` | body | `array<object>` | yes | This is the list of assistants that make up the squad.  The call will start with the first assistant in the list. |
| `members[]` | body | `array<object>` | yes | This is the list of assistants that make up the squad.  The call will start with the first assistant in the list. |
| `membersOverrides` | body | `object` | no | — |
