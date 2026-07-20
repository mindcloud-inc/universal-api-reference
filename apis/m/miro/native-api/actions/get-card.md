# Get Card with Miro

Retrieves a card from Miro.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/:board_id/cards/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Get Card](https://developers.miro.com/reference/get-card-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
