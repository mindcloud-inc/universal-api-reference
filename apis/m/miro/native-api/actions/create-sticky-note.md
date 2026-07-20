# Create Sticky Note with Miro

Creates a new sticky note in Miro.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards/:board_id/sticky_notes`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Create Sticky Note](https://developers.miro.com/reference/create-sticky-note-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `data.content` | body | `string` | yes | Text content for the sticky note |
