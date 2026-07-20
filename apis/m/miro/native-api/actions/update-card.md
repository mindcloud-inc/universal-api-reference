# Update Card with Miro

Updates an existing card in Miro.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/boards/:board_id/cards/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Update Card](https://developers.miro.com/reference/update-card-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
