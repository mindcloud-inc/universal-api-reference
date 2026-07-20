# Update Text with Miro

Updates an existing text item in Miro.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/boards/:board_id/texts/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Update Text](https://developers.miro.com/reference/update-text-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
