# List Records with OneDeck

Retrieves records from a specific OneDeck board.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/{{boardId}}/records`
- **Base URL:** `https://{accountName}.onedeck.com/api/v1`
- **Official documentation:** [List Records](https://www.onedeck.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | path | `string` | yes | The OneDeck board ID. |
| `filtersJson` | query | `string` | no | Optional JSON array for the docs filters parameter. |
