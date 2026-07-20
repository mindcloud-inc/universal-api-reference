# Create Card with Miro

Creates a new card in Miro.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards/:board_id/cards`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Create Card](https://developers.miro.com/reference/create-card-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `data.title` | body | `string` | yes | Title text for the new card |
