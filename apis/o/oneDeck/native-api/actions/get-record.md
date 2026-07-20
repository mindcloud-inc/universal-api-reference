# Get Record with OneDeck

Retrieves a record from a specific OneDeck board.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/{{boardId}}/records/{{recordId}}`
- **Base URL:** `https://{accountName}.onedeck.com/api/v1`
- **Official documentation:** [Get Record](https://www.onedeck.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | path | `string` | yes | The OneDeck board ID. |
| `recordId` | path | `string` | yes | The OneDeck record ID. |
