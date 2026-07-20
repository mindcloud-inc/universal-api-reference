# List Board Fields with OneDeck

Retrieves fields from a specific OneDeck board.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/{{boardId}}/fields`
- **Base URL:** `https://{accountName}.onedeck.com/api/v1`
- **Official documentation:** [List Board Fields](https://www.onedeck.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | path | `string` | yes | The OneDeck board ID. |
