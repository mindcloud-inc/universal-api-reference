# List Card Comments with Kanban Zone

Retrieves comments for a Kanban Zone card.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards/:id/comments`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [List Card Comments](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The unique identifier of the card. |
