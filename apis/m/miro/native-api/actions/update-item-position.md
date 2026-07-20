# Update Item Position with Miro

Updates an item's position or parent in Miro.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/boards/:board_id/items/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Update Item Position](https://developers.miro.com/reference/update-item-position-or-parent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
