# Get Account with Bridge

Retrieves an account from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/aggregation/accounts/:id`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Get Account](https://docs.bridgeapi.io/reference/getaccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `id` | path | `number` | yes | — |
