# Get Item with Miro

Retrieves an item from a Miro board.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/:board_id/items/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Get Item](https://developers.miro.com/reference/get-specific-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
