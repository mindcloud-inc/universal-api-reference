# Create Squad with Vapi

Creates a new squad in Vapi.

## Endpoint

- **Method:** `POST`
- **Path:** `/squad`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Create Squad](https://docs.vapi.ai/api-reference/squads/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | This is the name of the squad. |
| `members[]` | body | `array<object>` | yes | This is the list of assistants that make up the squad.  The call will start with the first assistant in the list. |
| `members[]` | body | `array<object>` | yes | This is the list of assistants that make up the squad.  The call will start with the first assistant in the list. |
| `members[]` | body | `array<object>` | yes | This is the list of assistants that make up the squad.  The call will start with the first assistant in the list. |
| `membersOverrides` | body | `object` | no | — |
