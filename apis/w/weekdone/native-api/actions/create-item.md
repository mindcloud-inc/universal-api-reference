# Create Item with Weekdone

Creates a new item in Weekdone.

## Endpoint

- **Method:** `POST`
- **Path:** `item`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Create Item](https://weekdone.com/developer#h-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | yes |
| `due_on` | body | `date` | no |
| `period` | body | `string` | no |
| `priority` | body | `number` | no |
| `private` | body | `number` | no |
| `source_id` | body | `string` | no |
| `team_id` | body | `number` | no |
| `type_id` | body | `number` | yes |
| `user_id` | body | `number` | no |
