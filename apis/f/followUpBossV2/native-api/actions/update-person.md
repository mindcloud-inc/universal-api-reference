# Update Person with Follow Up Boss

Updates an existing person in Follow Up Boss.

## Endpoint

- **Method:** `PUT`
- **Path:** `people/:id`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [Update Person](https://docs.followupboss.com/reference/people-id-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The person ID. |
| `mergeTags` | query | `boolean` | no | — |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `stage` | body | `string` | no | — |
| `assignedTo` | body | `string` | no | — |
| `assignedUserId` | body | `number` | no | — |
| `assignedLenderName` | body | `string` | no | — |
| `assignedLenderId` | body | `number` | no | — |
| `contacted` | body | `boolean` | no | — |
| `emails[].value` | body | `string` | no | — |
| `emails[].type` | body | `string` | no | — |
| `emails[].isPrimary` | body | `boolean` | no | — |
| `phones[].value` | body | `string` | no | — |
| `phones[].type` | body | `string` | no | — |
| `phones[].isPrimary` | body | `boolean` | no | — |
| `addresses[].type` | body | `string` | no | — |
| `addresses[].street` | body | `string` | no | — |
| `addresses[].city` | body | `string` | no | — |
| `addresses[].state` | body | `string` | no | — |
| `addresses[].code` | body | `string` | no | — |
| `addresses[].country` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | — |
