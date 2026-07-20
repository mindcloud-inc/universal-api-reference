# Update Record with OneDeck

Updates an existing record in a OneDeck board.

## Endpoint

- **Method:** `PUT`
- **Path:** `/boards/{{boardId}}/records/{{recordId}}`
- **Base URL:** `https://{accountName}.onedeck.com/api/v1`
- **Official documentation:** [Update Record](https://www.onedeck.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | path | `string` | yes | The OneDeck board ID. |
| `recordId` | path | `string` | yes | The OneDeck record ID. |
| `updatesJson` | body | `string` | yes | JSON array of OneDeck update objects with fieldId and value. |
