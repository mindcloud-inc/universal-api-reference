# Get Stock with Bridge

Retrieves a stock from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/aggregation/stocks/:id`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Get Stock](https://docs.bridgeapi.io/reference/getstock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `id` | path | `number` | yes | — |
