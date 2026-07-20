# Get Item with Bridge

Retrieves an item from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/aggregation/items/:id`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Get Item](https://docs.bridgeapi.io/reference/getitem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `id` | path | `number` | yes | — |
