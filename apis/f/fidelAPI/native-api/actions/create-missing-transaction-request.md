# Create Missing Transaction Request with Fidel API

Creates a missing transaction request in Fidel API.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards/:cardId/missing-transaction-requests`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Create Missing Transaction Request](https://reference.fidel.uk/reference/create-missing-transaction-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | — |
| `locationId` | body | `string` | yes | The ID of the location. |
| `amount` | body | `number` | yes | Transaction amount in the base currency. |
| `transactionDate` | body | `string` | yes | Transaction date in YYYY-MM-DD format. |
