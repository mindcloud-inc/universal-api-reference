# Create Text with Miro

Creates a new text item in Miro.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards/:board_id/texts`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Create Text](https://developers.miro.com/reference/create-text-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `data.content` | body | `string` | yes | Text content for the text item |
