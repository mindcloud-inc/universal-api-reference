# Remove Board Member with Miro

Removes a board member from Miro.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/boards/:board_id/members/:board_member_id`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [Remove Board Member](https://developers.miro.com/reference/remove-board-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `string` | no | Target board ID. |
| `board_member_id` | path | `string` | no | Target board member ID. |
