# Create Board with Miro

Creates a new board in Miro.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Create Board](https://developers.miro.com/reference/create-board)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Board name |
| `description` | body | `string` | no | Optional board description |
