# Create Objective with Weekdone

Creates a new objective in Weekdone.

## Endpoint

- **Method:** `POST`
- **Path:** `objective`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Create Objective](https://weekdone.com/developer#h-objectives)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `department_id` | body | `number` | no |
| `description` | body | `string` | yes |
| `period` | body | `string` | no |
| `team_id` | body | `number` | no |
| `type` | body | `string` | yes |
| `user_id` | body | `number` | no |
