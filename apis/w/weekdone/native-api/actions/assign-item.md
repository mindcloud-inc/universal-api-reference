# Assign Item with Weekdone

Assigns an item to a user in Weekdone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `item/:itemId/assign`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Assign Item](https://weekdone.com/developer#h-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `itemId` | path | `number` | yes |
| `user_id` | body | `number` | yes |
