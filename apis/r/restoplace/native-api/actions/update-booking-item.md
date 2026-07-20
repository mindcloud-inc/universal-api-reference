# Update Booking Item with Restoplace

Updates an existing booking item in Restoplace.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:id`
- **Base URL:** `https://api.restoplace.cc`
- **Official documentation:** [Update Booking Item](https://restoplace.cc/help/API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique Restoplace booking item ID. |
| `type` | body | `string` | no | Booking item type from the List Item Types action. |
| `floorid` | body | `number` | no | Hall ID that owns the booking item. |
| `number` | body | `string` | no | Visible item number. |
| `count_min` | body | `number` | no | Minimum guest capacity. |
| `count_max` | body | `number` | no | Maximum guest capacity. |
| `text` | body | `string` | no | Booking item description or comment. |
| `checked` | body | `number` | no | Whether the booking item is enabled. |
| `reserve` | body | `number` | no | Whether guests can book the item through the widget. |
| `group_reserve` | body | `number` | no | Whether the item is available for group reservations. |
| `view_only_hostess` | body | `number` | no | Whether the item is visible only to staff. |
