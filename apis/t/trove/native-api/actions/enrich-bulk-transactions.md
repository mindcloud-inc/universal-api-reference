# Enrich Bulk Transactions with Trove

Creates a bulk transaction enrichment request in Trove.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/bulk`
- **Base URL:** `https://trove.headline.com/api/v1`
- **Official documentation:** [Enrich Bulk Transactions](https://trove.headline.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactions[]` | body | `array<object>` | yes | Array of transactions to enrich in bulk. |
| `transactions[].description` | body | `string` | yes | The original transaction description string. |
| `transactions[].amount` | body | `number` | yes | Transaction value in the original currency. |
| `transactions[].date` | body | `date` | yes | The transaction date in YYYY-MM-DD format. |
| `transactions[].user_id` | body | `string` | yes | A unique identifier for the customer/user that performed this transaction. |
