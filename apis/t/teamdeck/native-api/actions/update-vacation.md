# Update Vacation with Teamdeck

Updates an existing vacation in Teamdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/vacations/:id`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Update Vacation](https://teamdeck.io/developers/api#operation/updateVacation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Teamdeck vacation ID. |
| `resource_id` | body | `number` | yes | — |
| `status` | body | `number` | no | — |
| `period_id` | body | `number` | no | — |
| `requested_approver_id` | body | `number` | no | — |
| `reason_id` | body | `number` | no | — |
| `description` | body | `string` | no | — |
| `external_id` | body | `string` | no | — |
| `start_date` | body | `string` | yes | — |
| `end_date` | body | `string` | yes | — |
