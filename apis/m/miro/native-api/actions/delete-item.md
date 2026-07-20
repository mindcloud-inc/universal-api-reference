# Delete Item with Miro

Deletes an item from a Miro board.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/boards/:board_id/items/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Delete Item](https://developers.miro.com/reference/delete-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
