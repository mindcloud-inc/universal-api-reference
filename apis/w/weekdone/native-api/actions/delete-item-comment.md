# Delete Item Comment with Weekdone

Deletes a comment from an item in Weekdone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `item/:itemId/comments/:commentId`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Delete Item Comment](https://weekdone.com/developer#h-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `commentId` | path | `number` | yes |
| `itemId` | path | `number` | yes |
