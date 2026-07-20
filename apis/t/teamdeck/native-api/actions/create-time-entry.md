# Create Time Entry with Teamdeck

Creates a new time entry in Teamdeck.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-entries`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Create Time Entry](https://teamdeck.io/developers/api#operation/addTimeEntry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resource_id` | body | `number` | yes |
| `status` | body | `number` | no |
| `project_id` | body | `number` | yes |
| `minutes` | body | `number` | yes |
| `weekend_booking` | body | `boolean` | no |
| `holidays_booking` | body | `boolean` | no |
| `vacations_booking` | body | `boolean` | no |
| `approver_id` | body | `number` | no |
| `description` | body | `string` | no |
| `external_id` | body | `string` | no |
| `start_date` | body | `string` | yes |
| `end_date` | body | `string` | yes |
