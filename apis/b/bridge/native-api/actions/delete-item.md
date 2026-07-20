# Delete Item with Bridge

Deletes an item from Bridge.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/aggregation/items/:id`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Delete Item](https://docs.bridgeapi.io/reference/deleteitem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `id` | path | `number` | yes | — |
