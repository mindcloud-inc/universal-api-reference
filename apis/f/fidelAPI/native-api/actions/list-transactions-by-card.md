# List Transactions by Card with Fidel API

Retrieves transactions for a Fidel card.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards/:cardId/transactions`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [List Transactions by Card](https://reference.fidel.uk/reference/list-transactions-by-card)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cardId` | path | `string` | yes |
