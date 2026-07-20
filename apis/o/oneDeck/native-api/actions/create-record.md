# Create Record with OneDeck

Creates a new record in a OneDeck board.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards/{{boardId}}/records`
- **Base URL:** `https://{accountName}.onedeck.com/api/v1`
- **Official documentation:** [Create Record](https://www.onedeck.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | path | `string` | yes | The OneDeck board ID. |
| `name` | body | `string` | yes | The name for the new record. |
| `fieldsJson` | body | `string` | no | Optional JSON array of field objects to include in the create payload. |
