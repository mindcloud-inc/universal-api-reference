# Update Item with Weekdone

Updates an existing item in Weekdone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `item/:itemId`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Update Item](https://weekdone.com/developer#h-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `due_on` | body | `date` | no |
| `itemId` | path | `number` | yes |
| `period` | body | `string` | no |
| `priority` | body | `number` | no |
| `type_id` | body | `number` | no |
