# List Cards with Kanban Zone

Retrieves cards from Kanban Zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [List Cards](https://docs.kanbanzone.io/apiReference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | query | `string` | yes | The board public ID. |
| `columns` | query | `string` | no | Comma-separated list of column IDs. |
| `daysSinceLastUpdate` | query | `number` | no | Filter by cards updated within the last N days. |
| `includeArchived` | query | `boolean` | no | Include archived cards in the response. |
