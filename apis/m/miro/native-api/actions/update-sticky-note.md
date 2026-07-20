# Update Sticky Note with Miro

Updates an existing sticky note in Miro.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/boards/:board_id/sticky_notes/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Update Sticky Note](https://developers.miro.com/reference/update-sticky-note-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
