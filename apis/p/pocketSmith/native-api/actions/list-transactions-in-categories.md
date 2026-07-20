# List Transactions In Categories with PocketSmith

Retrieves transactions for PocketSmith categories.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories/:id/transactions`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [List Transactions In Categories](https://developers.pocketsmith.com/reference/get_categories-id-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A comma-separated list of PocketSmith category IDs. |
