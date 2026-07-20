# Create Vacation with Teamdeck

Creates a new vacation in Teamdeck.

## Endpoint

- **Method:** `POST`
- **Path:** `/vacations`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Create Vacation](https://teamdeck.io/developers/api#operation/addVacations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resource_id` | body | `number` | yes |
| `status` | body | `number` | no |
| `period_id` | body | `number` | no |
| `requested_approver_id` | body | `number` | no |
| `reason_id` | body | `number` | no |
| `description` | body | `string` | no |
| `external_id` | body | `string` | no |
| `start_date` | body | `string` | yes |
| `end_date` | body | `string` | yes |
