# Get Sticky Note with Miro

Retrieves a sticky note from Miro.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/:board_id/sticky_notes/:item_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Get Sticky Note](https://developers.miro.com/reference/get-sticky-note-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `item_id` | path | `string` | no | Target item ID. |
