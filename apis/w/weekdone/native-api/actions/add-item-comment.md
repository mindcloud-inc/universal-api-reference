# Add Item Comment with Weekdone

Creates a comment on an item in Weekdone.

## Endpoint

- **Method:** `POST`
- **Path:** `item/:itemId/comments`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Add Item Comment](https://weekdone.com/developer#h-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `comment` | body | `string` | yes |
| `itemId` | path | `number` | yes |
