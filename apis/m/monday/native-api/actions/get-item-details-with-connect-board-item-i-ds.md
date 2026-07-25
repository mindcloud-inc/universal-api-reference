# Get Item Details with Connect Board Item ID's with Monday

Retrieves item details and linked board items from Monday.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.monday.com/v2/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | body | `number` | yes | Send multiple values as a array. |
| `includeMirrors` | body | `boolean` | no | If the column is a mirror, get the value from the destination board |
| `linkedBoardId` | body | `string` | yes | — |
| `connectColumnId` | body | `string` | yes | — |
