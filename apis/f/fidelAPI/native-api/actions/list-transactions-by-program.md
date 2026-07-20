# List Transactions by Program with Fidel API

Retrieves transactions for a Fidel program.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/:programId/transactions`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [List Transactions by Program](https://reference.fidel.uk/reference/list-transactions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `programId` | path | `string` | yes |
