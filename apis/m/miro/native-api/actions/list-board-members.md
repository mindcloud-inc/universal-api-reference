# List Board Members with Miro

Retrieves board members from Miro.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/:board_id/members`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [List Board Members](https://developers.miro.com/reference/get-board-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
