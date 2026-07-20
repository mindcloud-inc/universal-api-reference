# List Accounts with Bridge

Retrieves accounts from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/aggregation/accounts`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [List Accounts](https://docs.bridgeapi.io/reference/getaccounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `item_id` | query | `number` | no | Filter accounts by item |
