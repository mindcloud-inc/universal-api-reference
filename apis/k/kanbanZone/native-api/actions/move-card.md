# Move Card with Kanban Zone

Moves a card in Kanban Zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards/:id/move`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Move Card](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Card number to move |
| `columnId` | body | `string` | yes | Destination column ID |
