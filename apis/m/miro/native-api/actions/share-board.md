# Share Board with Miro

Shares a board with a member in Miro.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards/:board_id/members`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Share Board](https://developers.miro.com/reference/share-board)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
