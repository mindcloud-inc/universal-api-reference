# Delete Text with Miro

Deletes an existing text item from Miro.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/boards/:board_id/texts/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Delete Text](https://developers.miro.com/reference/delete-text-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
