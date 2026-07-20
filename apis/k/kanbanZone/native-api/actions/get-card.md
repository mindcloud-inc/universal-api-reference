# Get Card with Kanban Zone

Retrieves a card from Kanban Zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards/:id`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Get Card](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the card. |
| `board` | query | `string` | no | The public ID of the board for mirrored cards. |
