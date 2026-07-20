# Create Card Comment with Kanban Zone

Creates a card comment in Kanban Zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards/:id/comments`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Create Card Comment](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The unique identifier of the card |
| `text` | body | `string` | yes | The content of the comment |
