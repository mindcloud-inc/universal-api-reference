# Get Text with Miro

Retrieves a text item from Miro.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/:board_id/texts/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Get Text](https://developers.miro.com/reference/get-text-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
