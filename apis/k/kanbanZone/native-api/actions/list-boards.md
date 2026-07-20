# List Boards with Kanban Zone

Retrieves boards from Kanban Zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [List Boards](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeArchived` | query | `boolean` | no | Include archived boards in the response. |
| `includeColumns` | query | `boolean` | no | Include columns for boards in the response. |
| `includeCustomFields` | query | `boolean` | no | Include custom fields for boards in the response. |
