# Delete Card with Miro

Deletes an existing card from Miro.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/boards/:board_id/cards/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Delete Card](https://developers.miro.com/reference/delete-card-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
