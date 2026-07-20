# Delete Sticky Note with Miro

Deletes an existing sticky note from Miro.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/boards/:board_id/sticky_notes/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Delete Sticky Note](https://developers.miro.com/reference/delete-sticky-note-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
