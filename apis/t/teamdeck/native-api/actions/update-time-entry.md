# Update Time Entry with Teamdeck

Updates an existing time entry in Teamdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/time-entries/:id`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Update Time Entry](https://teamdeck.io/developers/api#operation/updateTimeEntry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Teamdeck time entry ID. |
| `resource_id` | body | `number` | yes | — |
| `status` | body | `number` | no | — |
| `project_id` | body | `number` | yes | — |
| `minutes` | body | `number` | yes | — |
| `weekend_booking` | body | `boolean` | no | — |
| `holidays_booking` | body | `boolean` | no | — |
| `vacations_booking` | body | `boolean` | no | — |
| `approver_id` | body | `number` | no | — |
| `description` | body | `string` | no | — |
| `external_id` | body | `string` | no | — |
| `start_date` | body | `string` | yes | — |
| `end_date` | body | `string` | yes | — |
