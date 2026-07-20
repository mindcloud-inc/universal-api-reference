# Get Board with Kanban Zone

Retrieves a board from Kanban Zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/board/:board`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Get Board](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | path | `string` | yes | The board public ID. |
| `includeColumns` | query | `boolean` | no | Include columns for the board in the response. |
| `includeCustomFields` | query | `boolean` | no | Include custom fields for the board in the response. |
