# List Transaction Accounts In User with PocketSmith

Retrieves transaction accounts for a PocketSmith user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/transaction_accounts`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [List Transaction Accounts In User](https://developers.pocketsmith.com/reference/get_users-id-transaction-accounts-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The unique identifier of the PocketSmith user. |
