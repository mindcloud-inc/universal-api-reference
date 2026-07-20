# List Webhooks with Kanban Zone

Retrieves webhooks from Kanban Zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [List Webhooks](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | query | `string` | yes | The public ID of the board. |
